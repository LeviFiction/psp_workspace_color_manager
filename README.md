# psp_workspace_color_manager
A test to see if it's possible to create a workspace color manager for PaintShop Pro

# Custom Theme Details

First test was to find out what Corel added when installing a custom theme color:
- Folder in ProgramData called "CustomTheme"
- A sub-folder for each theme
- A config.ini
  - Localized strings for the theme name name in different languages
  - Theme type: 0=dark, 1=light, or 2=grey
- A Registry file containing over 2851 lines
- A quick examination of the colors used suggests there are only 185 distinct colors.  But quite a lot of places where colors are set

TODO: Perform a thorough analysis of each type of item and where colors repeat.  Also how closely colors match each other for things like shadows and separators
See if there is a good way to calculate some of those from a subset of colors.  How detailed do we want this?  

Example of color registery keys
"3DHighlight"=dword:
"AboutBox - Background"=dword:
"ActiveButtonColor1"=dword:
"ActiveButtonColor2"=dword:
"Adjut Group Background"=dword:
"Adjut Group Separator"=dword:
"Button - Background1"=dword:
"Button - Background1 - Checked"=dword:
"CheckBox - Text"=dword:
"ComboBox - Background1"=dword:
"ComboBox - Background2"=dword:
"ComboBox - Background2 - Over"=dword:
"ComboBox - Border"=dword:
"ComboBox - Border - Disabled"=dword:
"ComboBox - Text"=dword:
"ComboBox - Text - Over"=dword:
"ComboBox - Text - Selected"=dword:
"ComboBoxItem - Background - DropdownOpened"=dword:
"ComboBoxItem - Background - Over"=dword:
"ComboBoxItem - Text"=dword:
"ComboBoxItem - Text - Selected"=dword:
"ContentControl - TopPanel - LargeIcon - Background1"=dword:
"ContentControl - TopPanel - LargeIcon - Background2"=dword:
"Control - JneBtn - Edit - Background"=dword:
"Control - JneBtn - METER - Background"=dword:
"Control - Rebar - H-Line1"=dword:
"Control - Rebar - H-Line2"=dword:
"Control - Rebar - V-Line1"=dword:
"Control - Rebar - V-Line2"=dword:

Next Tests and Discoveries:
- Can I move CustomTheme folder - RESULTS: NO
- Can I re-create this without the custom theme option in prior versions of PSP?
- Can I get PSP to recognize and allow my custom themes?
- Can I create custom themes and get them to load dynamically?
