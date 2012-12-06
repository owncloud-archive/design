Application Administration Mockup
==================================

Introduction
------------

The new application administration page has been streamlined and simplified. The new interface includes a better user experience allowing for apps to be enabled 
and disabled by dragging between the two sections or by the press of a button. Apps can also be installed by dragging and dropping an application .zip archive 
into the browser window. The ownCloud app directory has also been integrated into the administration panel and allows for apps to be installed with one click.

The interface is designed with multiple screen sizes in mind. Application tiles are rearranged as needed to best fit. For example, larger screens may have more 
than four tiles per row.

Figure 1 – App panel with no apps installed
--------------------------------------------

When there are no apps to display, the administration panel directs the user to install an app through the app market or by dragging and dropping apps into the
 browser window. This view will be rarely seen as ownCloud is bundled with apps.

Figure 2 – App panel with apps installed
----------------------------------------

Applications are divided into enabled and disabled categories, of which both can be collapsed (see **Figure 10**). Each application tile includes the application 
title, developer, version, and an icon. Application tiles can be dragged between the enabled and disabled categories to change the state of the app to correspond 
to the respective category. An icon also appears upon hover to disable or enable the app (see **Figure 7**).

“Get Apps” opens the app market within the administration panel (see **Figure 8**). “Create App” opens the ownCloud documentation on app development. This behavior 
is similar to that of the current admin panel. There is also a help button to display information regarding app installation (see **Figure 6**) similar to the 
information displayed when no apps are installed (see **Figure 1**).

Figure 3 – Enabled app info pane
--------------------------------

Clicking on an app’s tile will bring up an application’s settings pane (see **Figure 4**). The user can view description and legal information by selecting the 
“Info” tab. The ability to disable the application is available on both tabs.

Internal applications are labeled as such in the bottom right corner.

Figure 4 – Enabled app settings pane
------------------------------------

The settings tab of the application information pane is used for settings that need to be handled by administrators. Settings in this section are designed in a 
global context. Application developers can specify and program a settings page for this panel. The settings tab opens by default.

Both enabled and disabled applications have a settings area.

Figure 5 – Disabled app info pane
---------------------------------

Disabled apps have a similar layout to their enabled app counterparts (see **Figure 3**). Disabled apps, however, can be uninstalled (deleted) from the web server. 

Settings can be modified when the application is disabled, too.

Figure 6 – Help pane
--------------------

The help pane can be accessed by selecting the help icon in the bottom right. The help pane is similar to that of **Figure 1**.

Figure 7 – Quick enable/disable
-------------------------------

To quickly enable or disable apps, an icon appears upon hovering over an app’s tile. In this case, the disable icon is displayed because the app is enabled.

Figure 8 – App market
---------------------

The app market is now located within the administration panel. The current app market found at `http://apps.owncloud.com/
<http://apps.owncloud.com/>`_ will remain active as this integrated app market uses the current market to grab application data. Apps, much like the current 
market, are organized by date added, alphabetical, rating, and downloads. The interface acts much like the installed app listing in grid view and features 
infinite scrolling. The main page also features applications selected by the ownCloud staff.

Users may also search for applications (see **Figure 9**).

Figure 9 – Detailed app view when browsing market (search results)
------------------------------------------------------------------

Upon selecting an application, the user sees the detailed view. This view shows version number, downloads, rating, and fan count. The application’s description 
and images (if available) are also found on this page. If an application is top rated or a staff pick, the appropriate badge is displayed at the bottom.

The user has the option to directly install the application to the ownCloud instance using the “Install” button. The user can also optionally download the 
application .zip using the appropriate button.

Note that comments and other advanced features found in the current market are not found in the integrated market. These features can be found using the 
“More Info” button.

Search results are delivered as expected and also features infinite scrolling.

Figure 10 – App panel with apps installed (collapsed)
-----------------------------------------------------

The enabled and disabled application sections can be collapsed. When collapsed, the section header has the number of applications hidden in parentheses.