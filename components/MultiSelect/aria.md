## Accessibility

The Telerik UI MultiSelect component is [WCAG 2.1 AAA](https://www.w3.org/TR/WCAG21/) and [Section 508](http://www.section508.gov/) compliant. The MultiSelect also follows the [WAI-ARIA best practices](https://www.w3.org/TR/wai-aria-practices/) for implementing the keyboard navigation for its component role, and is tested against the popular screen readers.

### Wai-Aria

**Container `k-multiselect-wrap`**

| Attribute|Usage|
|---------------------|---------------------|
|`role=combobox`|Announces the presence of a textbox as inner element of the multiselect used for filtering. |
|`aria-expanded`| Announces the state of the visibility of the popup. |
|`aria-haspopup="listbox"`| Indicates the presence of a listbox popup. |
|`aria-owns="[POPUP_ID]"`| Points to the popup element. Builds relationship between the input and the popup.  |

**Input**

| Attribute|Usage|
|---------------------|---------------------|
|`role=textbox`|Announces the presence of a textbox as inner element of the multiselect used for filtering. |
|`aria-autocomplete="list"`| Attribute is rendered and value is set to list when **filtering** feature is enabled. |
|`aria-describedby="[TAGLIST_ID]"`| Points to the taglist element that contains the selected items.  |
|`aria-controls="[POPUP_LISTBOX_ID]"`| Points to the popup element. Builds relationship between the input and the popup.  |
|`aria-activedescendent=[COMPONENT_ID]`| Points to the focused item. Either an item from the popup, or a tag item from the selected items. The focused item is changed via keyboard navigation. |
|`aria-disabled="true"`|Attribute is rendered only when the multiselect is disabled.|
|`aria-invalid="true"`|Attribute is rendered only when the multiselect is in form and announces the valid state of the component.|

**ListBox Popup**

| Attribute|Usage|
|---------------------|---------------------|
|`role=listbox`|Identifies the ul element as a listbox. |
|`aria-labelledby=[ARIALABELLEDBY_OPTION]`| Provides a label for the listbox of the multiselect as well. |
|`aria-label=[PLACEHOLDER_OPTION]`|If aria-labelledby configuration option is not passed to the MultiSelect, it sets aria-label with value of the placeholder option. |
|`aria-multiselectable="true"`| Announces multiselection of the listbox popup.  |

**ListBox Popup Item**

| Attribute|Usage|
|---------------------|---------------------|
|`role=option`|Identifies the li element as a listbox option. |
|`aria-selected=true`| Indicates the selected state of the item. Attribute is not rendered when the item is not selected. |

### Testing

Pages used for testing could be found in this repository: https://github.com/telerik/blazor-ui/accessibilityPages

The tool used for Automated Testing is [Selenium.Axe](https://www.nuget.org/packages/Selenium.Axe/).

Any Accessibility Issues could be reported in Telerik Support System.

## Resources

https://www.w3.org/TR/wai-aria-practices/#combobox
https://www.w3.org/TR/wai-aria-practices/examples/combobox/aria1.1pattern/listbox-combo.html
https://www.w3.org/TR/wai-aria-practices/#listbox_kbd_interaction