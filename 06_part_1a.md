# 5. User Interface Components

#### [5.1. ](https://vaadin.com/book/vaadin6/-/page/components.html#components.overview)General

A component is a visual item on the screen. A component can be a button, a textfield or some more complex item like a panel which contains other components.

The following attributes can be set for each component:

-         id

-         name

The id attribute must be unqiue within the window component (see section Components collection). This becomes an important factor when dealing with event handling. We advise you to follow the Java identifiers naming convention when providing value to the id.

Which means, an id can contain digits, letters, underscores (_) and dollar signs ($), but it must not start with digits. The first letter should be lowercase and internal words should start with a capital letter. It should also be short yet meaningful.

The name attribute is used for the following purposes:

-         data mapping, for example: Consider the scenaro where a panel component has the name attribute called "employee". Within the panel component there are 2 textfield components which also have the name attribute with values as “name” and “department”. When a data object with properties called “name” and “department” is set to the panel component using the panel component's name attribute value as the reference, the textfield component with the name attribute value as “name” is mapped to the property called “name” of the data object and the same happens for the other component with the name attribute value as “department”.

-         grouping of components, for example: Consider when 2 button components have different ids as "btnNextTop" and “btnNextBottom” and with same name - “btnNext”. An “onclick” event is defined for “btnNext” (name attribute of the button components). The click on one of these buttons will trigger the event defined.

**Note: the id and name attributes are case-sensitive.**

The following section will describe all the components and its attributes and elements. There is a difference between attributes and elements when declaring QAML (QAfe Markup Language), the example below explains:

<choice tooltip="Please select your country”>

<choice-item displayname="The Netherlands” value=”NL”/>

<choice-item displayname="Belgium” value=”BE”/>

</choice>

 

The above lines of code can be interpreted as follows:

Choice: component tagname

-         Tooltip: attribute of the component

-         Choice-Item: element of the component

`o`        Displayname: attribute of the element

`o`        Value: attribute of the element

[5.2. Interfaces and Abstractions](https://vaadin.com/book/vaadin6/-/page/components.interfaces.html)

[5.3. Common Component Features](https://vaadin.com/book/vaadin6/-/page/components.features.html)

#### 5.4. Label

Displays a single-line of noneditable text.

 

Tagname: **_label_**

 

Example:

              ![image alt text](assets/images/image_6_0.png?raw=true)

 

              qaml code:

`<label` `displayname="This Label displays plain text."/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as label.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
</table>


 

 

#### 5.5. Link

Looks like a label which is rendered like a hyperlink.

 

Tagname: **_link_**

 

Example:

              ![image alt text](assets/images/image_6_1.png?raw=true)

 

              qaml code:

`<link` `displayname="Hyperlink"/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hyperlink.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
</table>


#### 5.6. TextArea

Displays a multi-line text frame which can be optionally editable. 

 

Tagname: **_textarea_**

 

Example:

              ![image alt text](assets/images/image_6_2.png?raw=true)

 

              qaml code:

              `<textarea` `rich="true"` `rows="5">`

           	             `<value>` `This is a multiline, editable textarea component.</value>`

              `</textarea>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as label.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to entered text.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>orientation</td>
    <td> </td>
    <td>leftright</td>
    <td>Specifies the position of the displayname attribute.
The possible values are:
-         leftright: placed left the component
-         updown: placed above the component
 </td>
  </tr>
  <tr>
    <td>required</td>
    <td> </td>
    <td>false</td>
    <td>If true, a missing or empty value causes a validation error.
 </td>
  </tr>
  <tr>
    <td>rich</td>
    <td> </td>
    <td>false</td>
    <td>If true, a toolbar with format controls will appear. These format controls gives a user the ability to change text characteristics. The following text characteristics are available : font family, color, size, and style, and other properties such as text alignment and bullets.
 </td>
  </tr>
  <tr>
    <td>rows</td>
    <td> </td>
    <td>1</td>
    <td>Specifies the number of lines which will be displayed. When the value attribute contains more lines than the rows attribute allows, a vertical scrollbar will appear.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
Indicates the entered text.</td>
  </tr>
</table>


 

#### 5.7. TextField

Displays a single-line text that is optionally editable. 

Tagname: **_textfield_**

 

Example:

              ![image alt text](assets/images/image_6_3.png?raw=true)

             

              qaml code:

`<textfield` `displayname="Name"` `orientation="updown">`

		`<value>This is a singleline, editable textfield component.</value>`

`</textfield>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as label.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to enter text.
 </td>
  </tr>
  <tr>
    <td>format</td>
    <td> </td>
    <td>dd/MM
/yyyy</td>
    <td>If the type attribute is set to "date", the format attribute is used to display date in a certain format.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>max-length</td>
    <td> </td>
    <td> </td>
    <td>Specifies the maximum number of characters to be entered.
Applicable to text values.
 </td>
  </tr>
  <tr>
    <td>max-value</td>
    <td> </td>
    <td>20</td>
    <td>Specifies the maximum value for this component.
Applicable to number values.
 </td>
  </tr>
  <tr>
    <td>validation-message</td>
    <td> </td>
    <td> </td>
    <td>Specifies the error message when there are no matches to the regular expression, see the regexp element.
 </td>
  </tr>
  <tr>
    <td>validation-title</td>
    <td></td>
    <td></td>
    <td>Specifies the error message dialog title when there are no matches to the regular expression, see the regexp element.</td>
  </tr>
  <tr>
    <td>validation-message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, Specifies the error message when there are no matches to the regular expression, see the regexp element.</td>
  </tr>
  <tr>
    <td>validation-title-key</td>
    <td></td>
    <td></td>
    <td>Is used for multi-language.
If set, Specifies the error message dialog title when there are no matches to the regular expression, see the regexp element.</td>
  </tr>
  <tr>
    <td>min-length</td>
    <td> </td>
    <td> </td>
    <td>Specifies the minimum number of characters to be entered.
Applicable to text values.
 </td>
  </tr>
  <tr>
    <td>min-value</td>
    <td> </td>
    <td>0</td>
    <td>Specifies the minimum value for this component.
Applicable to number values.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>orientation</td>
    <td> </td>
    <td>leftright</td>
    <td>Specifies the position of the displayname attribute.
The possible values are:
-         leftright: placed left the component
-         updown: placed above the component
 </td>
  </tr>
  <tr>
    <td>required</td>
    <td> </td>
    <td>false</td>
    <td>If true, a missing or empty value causes a validation error.
 </td>
  </tr>
  <tr>
    <td>suggest</td>
    <td> </td>
    <td>false</td>
    <td>If true, auto completion is on. The auto complete functionality tries to dynamically predict a word or phrase which the user started to type before the user actually types this word or phrase completely.

When set suggestions, a datamodel of the selected suggestion is attached internally.

<!-- Triggered by the onChange listener-type -->
<!-- suggestionResult: list of records,
each record contains ADDRESS, ADDRESS_ID and other fields -->
<set component-id="<textfieldID>" ref="suggestionResult">
  <mapping key="value" value="ADDRESS"/>
</set>

Access the value and datamodel:

<!--The value -->
<store name="textfieldValue" ref="<textfieldID>" src="component"/>

<!--The datamodel -->
<store name="textfieldDatamodel" ref="<textfieldID>$DATA" src="pipe"/>

<!--Members of the datamodel -->
<store name="textfieldDatamodelAddressID" ref="<textfieldID>$DATA.ADDRESS_ID" src="pipe"/>
<store name="textfieldDatamodelAddress" ref="<textfieldID>$DATA.ADDRESS" src="pipe"/>
 </td>
  </tr>
  <tr>
    <td>suggest-chars</td>
    <td> </td>
    <td>3</td>
    <td>If the suggest attribute is set to true, this attribute specifies the number of characters entered whereupon auto completion is activated. After entering this number of characters an onchange event will be triggered which handles the auto completion mechanism.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>type</td>
    <td> </td>
    <td>Text</td>
    <td>Specifies the type of the value attribute.
The possible types are:
-         text: can be anything
-         chars: accepts characters only, so no numbers are allowed
-         int: accepts integers only
-         signed_int: accepts positive integers only, so >=0
-         double: accepts numbers only
-         date: accepts dates only, become a date component
-         email: accepts valid email addresses only
-         spinner: accept integers only, between the min-value and max-value attributes
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>True</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
Indicates the entered text.</td>
  </tr>
  <tr>
    <td>regexp</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
Lets you use a regular expression to validate the entered text.</td>
  </tr>
</table>


#### 5.8. Password

Does not display entered text, instead, each text character entered will appear as a bullet.

 

Tagname: **_password_**

 

Example:             

![image alt text](assets/images/image_6_4.png?raw=true)

 

qaml code:

`<label` `displayname="This is a passwordfield"/>`

`<password id="passwordField"></password>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as label.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to enter text.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>orientation</td>
    <td> </td>
    <td>leftright</td>
    <td>Specifies the position of the displayname attribute.
The possible values are:
-         leftright: placed left the component
-         updown: placed above the component
 </td>
  </tr>
  <tr>
    <td>password-mask</td>
    <td> </td>
    <td> </td>
    <td>Specifies a mask for the input text.
 </td>
  </tr>
  <tr>
    <td>required</td>
    <td> </td>
    <td>false</td>
    <td>If true, a missing or empty value causes a validation error.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
Indicates the entered text.</td>
  </tr>
</table>


           	          	            

           

#### Slider

Lets the user select a value by moving a slider thumb between the start and end points of a slider track. The slider track is setup according to the min-ticks and max-ticks attributes.

 

Tagname: **_slider_**

 

Example:

![image alt text](assets/images/image_6_5.png?raw=true)

 

              qaml code:

`<slider` `max-ticks="100"` `min-ticks="0"` `tickSize="10"`  `width="300px"/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as label.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>max-ticks</td>
    <td> </td>
    <td> </td>
    <td>Specifies a number for the end point.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>min-ticks</td>
    <td> </td>
    <td> </td>
    <td>Specifies a number for the start point.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>ticksize</td>
    <td> </td>
    <td> </td>
    <td>The spacing of the tick marks relative to the end point.
 </td>
  </tr>
  <tr>
    <td>tick-labels</td>
    <td></td>
    <td>2</td>
    <td>Specifies the number of labels to be shown including the min and max ticks. The value must be equals or greater than 2.</td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>value</td>
    <td></td>
    <td></td>
    <td>Element which has no attributes.
Indicates the value which is between the min and max ticks.</td>
  </tr>
</table>


[5.10. Date and Time Input with ](https://vaadin.com/book/vaadin6/-/page/components.datefield.html)[DateField](https://vaadin.com/book/vaadin6/-/page/components.datefield.html)

#### Dropdown

#### **Dropdown**

Contains a drop-down list from which the user can select a single value.

The list is composed of one or more *item* elements.

 

Tagname: **_dropdown_**

 

Example:

![image alt text](assets/images/image_6_6.png?raw=true)

 

qaml code:

`<dropdown` `id="myDropdown">`

           	             `<item` `displayname="Visa"` `value="visa"/>`

           	             `<item` `displayname="MasterCard"` `value="master-card"/>`

           	             `<item` `displayname="American Express"` `value="american-express"/>`

`</dropdown>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the component is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>empty-item-displayname</td>
    <td> </td>
    <td> </td>
    <td>Specifies the text to appear as the first item in the list.</td>
  </tr>
  <tr>
    <td>empty-item-message-key</td>
    <td> </td>
    <td> </td>
    <td>
Is used for multi-language text fields.
If set, the empty-item-displayname attribute will be replaced by the value of the key in the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>empty-item-value</td>
    <td> </td>
    <td> </td>
    <td>Indicates the (internal) value of the empty-item-displayname attribute.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>required</td>
    <td> </td>
    <td>false</td>
    <td>If true, a missing or empty value causes a validation error.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>tooltip</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as hint.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the component.
If false, the component is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>item</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
A dropdown list can be composed by defining one or more item elements.</td>
  </tr>
</table>


 

 

Attributes of **_item_** element:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>contextmenu</td>
    <td> </td>
    <td> </td>
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined as a menu-definition.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to display as label of the item.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the item.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used as a multi-language key.
If set, the displayname attribute will be replaced by the corresponding value of the key in the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>selected</td>
    <td> </td>
    <td>false</td>
    <td>If true, the item is selected.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the item.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Indicates the (internal) value of the item.
 </td>
  </tr>
</table>


