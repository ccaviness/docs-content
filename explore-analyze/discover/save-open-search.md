---
navigation_title: Save a search for reuse
mapped_pages:
  - https://www.elastic.co/guide/en/kibana/current/save-open-search.html
applies_to:
  stack: ga
  serverless: ga
products:
  - id: kibana
description: Save Discover sessions to reuse searches, queries, and configured views. Add saved searches to dashboards or use them as a foundation for building visualizations.
---

# Save a search for reuse [save-open-search]

Saved **Discover** sessions preserve your queries, filters, column selections, and view configurations for reuse. Save sessions to return to specific data explorations, share search results with team members, add searches to dashboards, or use them as a foundation for building visualizations. This guide shows how to save, reopen, duplicate, and manage Discover sessions.

## Requirements [save-search-requirements]

To save searches, you need **Create** and **Edit** permissions for the {{saved-objects-app}} feature in {{product.kibana}}. If you don't have these permissions, the **Save** button won't be visible. For more information, refer to [Read-only access](#discover-read-only-access).


### Read-only access [discover-read-only-access]

If you don’t have sufficient privileges to save Discover sessions, the following indicator is displayed and the **Save** button is not visible. For more information, refer to [Granting access to {{kib}}](elasticsearch://reference/elasticsearch/roles.md).

:::{image} /explore-analyze/images/kibana-read-only-badge.png
:alt: Example of Discover's read only access indicator in the {{product.kibana}} header
:screenshot:
:::


## Save a Discover session [_save_a_discover_session]

By default, a Discover session stores the query text, filters, and current view of **Discover**, including the columns and sort order in the document table, and the {{data-source}}.

1. Once you’ve created a view worth saving, click **Save** in the application menu.
2. Enter a name for the session.
3. Optionally store [tags](../find-and-organize/tags.md) and the time range with the session.
4. Click **Save**.
5. To reload your search results in **Discover**, click **Open** in the application menu, and select the saved Discover session.

If the saved Discover session is associated with a different {{data-source}} than is currently selected, opening the saved Discover session changes the selected {{data-source}}. The query language used for the saved Discover session is also automatically selected.



## Duplicate a Discover session [_duplicate_a_discover_session]

1. In **Discover**, open the Discover session that you want to duplicate.
2. In the application menu, click **Save**.
3. Give the session a new name.
4. Turn on **Save as new Discover session**.
5. Click **Save**.


## Add search results to a dashboard [_add_search_results_to_a_dashboard]

Add the current Discover session to a dashboard as a new panel. You can save the table directly from the Discover toolbar, or add a previously saved Discover session from the dashboard library.

### Save the table directly from Discover [save-table-to-dashboard]
```{applies_to}
stack: ga 9.4
serverless: ga
```

Save the current view of the documents table to a new or existing dashboard without first saving the Discover session to the library. The resulting panel stores its configuration with the dashboard, so later changes to the Discover session don't affect the panel.

To use this option, you need permission to view and create dashboards. The button isn't available when you're editing Discover inline from another app, such as the dashboard embeddable editor.

1. In the documents table toolbar, select {icon}`dashboardApp` **Save table to dashboard**.
2. Enter a title for the panel, and optionally a description.
3. Under **Add to dashboard**, select **New** to create a dashboard, or **Existing** to pick one from the list.
4. Select **Save and go to Dashboard**.

### Add a saved Discover session from the library [add-discover-session-from-library]

1. Save the Discover session following the steps in [Save a Discover session](#_save_a_discover_session).
2. Go to **Dashboards**.
3. Open or create the dashboard, then select **Edit**.
4. Select **Add from library**.
5. From the **Types** dropdown, select **Discover session**.
6. Select the Discover session that you want to add, then select **X** to close the list.
