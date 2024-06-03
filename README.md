<b>Hide Firefox UI Elements (Top Bar and Bookmarks Sidebar) - CSS File</b>
<br><br>
This CSS file is designed to customize the Firefox browser's appearance by hiding the top bar (which includes the tab bar and address bar) and the bookmarks sidebar. By applying this CSS, you can achieve a cleaner and more minimalistic browsing interface. This can be particularly useful for users who prefer a distraction-free environment or want to maximize screen real estate.
<br><br><br>
<b>Features</b>
<br><br><b>Hide Top Bar:</b> Removes the entire top bar, including the tab bar and address bar.<br>
<b>Hide Bookmarks Sidebar:</b> Completely hides the bookmarks sidebar for a cleaner look.
<br><br><br>
<b>Usage Instructions</b>
<br><br>
<b>1. Locate Firefox Profile Folder:</b><br>
   <ul>
   <li>Open Firefox.<br>
   <li>Type <b>about:support</b> in the address bar and press Enter.<br>
   <li>Under the "Application Basics" section, find "Profile Folder" and click "Open Folder."<br><br>
   </ul>

<b>2. Create or Edit UserChrome.css:</b><br>
   <ul>
   <li>In the profile folder, create a new folder named <b>chrome</b> if it doesn't already exist.<br>
   <li>Inside the chrome folder, create a new file named <b>userChrome.css</b> if it doesn't already exist.<br><br>
   </ul>

<b>3. Add CSS Code:</b><br>
   <ul>
   <li>Open the <b>userChrome.css</b> file with a text editor.<br>
   <li>Copy and paste the following CSS code into the file:<br><br>
   </ul>

``` Css
.browserStack {
  position: absolute !important;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

#TabsToolbar {
  background-color: #222222FF !important;
  border-radius: 0px 0px 0px 0px !important;
}

.devtools-toolbox-bottom-iframe {
  position: absolute;
}

#navigator-toolbox {
  position: absolute;
  margin-top: -70px;
  opacity: 0;
  transition: all 200ms;
  z-index: 2;
  width: 100%;
}
 
#navigator-toolbox:hover {
  position: absolute;
  margin-top: 0px;
  opacity: 1;
  transition: all 200ms;
  transition-delay: 100ms;
}

#main-window[sizemode="maximized"] #navigator-toolbox {
  position: absolute;
  margin-top: -84px;
  opacity: 1;
  transition: all 200ms;
}
 
#main-window[sizemode="maximized"] #navigator-toolbox:hover {
  position: absolute;
  margin-top: 0px;
  opacity: 1;
  transition: all 200ms;
  transition-delay: 100ms;
}

#sidebar-box {
  display: flex !important;
  flex-direction: column !important;
  position: absolute !important;
  max-width: 270px !important;
  min-width: 270px !important;
  width: 270px !important;
  left: auto !important;
  right: -260px !important;
  top: 0 !important;
  bottom: 0 !important;
  background-color: #303030FF !important;
  z-index: 1 !important;
  transition: all 200ms;
  opacity: 0;
}

#sidebar-box:hover {
  right: 0px !important;
  opacity: 1;
  transition: all 200ms;
  transition-delay: 100ms;
}

#main-window[sizemode="maximized"] #sidebar-box {
  max-width: 270px !important;
  min-width: 270px !important;
  transition: all 200ms;
  background-color: #303030FF !important;
  display: flex !important;
  position: absolute !important;
  width: 270px !important;
  left: auto !important;
  right: -269px !important;
  top: 0 !important;
  bottom: 0 !important;
  flex-direction: column !important;
  z-index: 1 !important;
}

#main-window[sizemode="maximized"] #sidebar-box:hover {
  right: 0px !important;
  transition: all 200ms;
  transition-delay: 100ms;
}

#sidebar-header {
  display: none;
}

#sidebar-splitter {
  display: none;
}

#main-window[sizemode="maximized"] #sidebar-splitter {
  display: none;
}

#bookmarks-view {
  font-size: 16px;
}

.bookmark-item[container], treechildren::-moz-tree-row {
  margin: 8px 0px 0px 0px !important;
}

.bookmark-item[container], treechildren::-moz-tree-image {
  width: 20px !important;
  height: 20px !important;
  padding-right: 10px !important;
}

```
   
<b>4. Restart Firefox:</b><br>
   <ul>
   <li>Save the <b>userChrome.css</b> file and restart Firefox for the changes to take effect.<br><br><br>
   </ul>
   
<b>Notes</b><br><br>
<b>Revert Changes:</b> To undo the changes, simply delete the userChrome.css file or remove the relevant CSS code.<br>
<b>Customization:</b> You can further customize the CSS to show or hide additional elements as needed.<br><br>

This CSS customization provides a simple way to tailor Firefox's interface to your personal preferences. Enjoy your streamlined browsing experience!
