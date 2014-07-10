# 6. User Interface Components

#### 6.1. General

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

#### 6.2. Interfaces and Abstractions

#### 6.3. Common Component Features

#### 6.4. Label

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


 

 

#### 6.5 Link

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


#### 6.6. TextArea

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


 

#### 6.7. TextField

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


#### 6.8. Password

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


           	          	            

           

#### 6.9 Slider

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


#### 6.10. Date and Time Input with DateField

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


#### 6.11. Button

Is a commonly used rectangular button which can trigger a click event. It can have a text, specified by the *displayname* attribute.

 

Tagname: **_button_**

 

Example:

![image alt text](assets/images/image_6_7.png?raw=true)             

 

qaml code:

`<button` `id="myButton"` `displayname="Default` *`Button"/*>`

 

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
    <td>Specifies the context menu associated with this component. It refers to a context menu which is defined using a menu-definition tag.
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
    <td>Text to display as label on the button.
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
    <td>image</td>
    <td></td>
    <td></td>
    <td>The location of an image to display on the button</td>
  </tr>
  <tr>
    <td>key</td>
    <td> </td>
    <td> </td>
    <td>Used for assigning a shortcut key.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used as a multi-language key.
If set, the displayname attribute will be replaced by the corresponding value of the key in the multi-language resource.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the component.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to be camel cased, like fontColor, instead of font-color.
 
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
    <td>Specifies the width of the component, usually in pixels.</td>
  </tr>
</table>


#### 6.12. CheckBox

#### **Checkbox**

Consists of an optional text and a small box which can toggle tick mark on clicks.

 

Tagname: **_checkbox_**

 

Example:

![image alt text](assets/images/image_6_8.png?raw=true)

 

qaml code:

`<checkbox` `id="myCheckbox"` `displayname="bread"/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>checked</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether a check mark is displayed on the checkbox.
If the check mark is set, the value of the the checkbox will be set to the checked-value attribute (if defined) or to true. Otherwise the value of the the checkbox will be set to the unchecked-value attribute (if defined) or to false"; toggle is dynamic, whereas the XML declaration declares an initial setting.
 </td>
  </tr>
  <tr>
    <td>checked-value</td>
    <td> </td>
    <td> </td>
    <td>Is used as the value of the component when the checked attribute is true.</td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.
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
    <td>*</td>
    <td> </td>
    <td>Text to display as label.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to toggle the check mark on or off.
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
    <td>Is used as a multi-language key.
If set, the displayname attribute will be replaced by the corresponding value of the key in the multi-language resource.
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
    <td>unchecked-value</td>
    <td> </td>
    <td> </td>
    <td>Is used as the value of the component when the checked attribute is false.
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


#### 6.13. Choice

Lets the user makes a single choice within a set of mutually exclusive choices.

It is composed of one or more *choice-item* elements.

 

Tagname: **_choice_**

 

Example:                        	          	          	          	          	          	          	          	          	          	            

![image alt text](assets/images/image_6_9.png?raw=true)

 

qaml code:

`<choice` `id="myChoice" horizontal="false">`

`<choice-item` `displayname="1942"/>`

`<choice-item` `displayname="1952"/>`

`<choice-item` `displayname="1962"/>`

`</choice>`

 

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
This is similar to the class attribute in HTML elements.
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
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to select a single choice.
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
    <td>horizontal</td>
    <td> </td>
    <td>true</td>
    <td>If true, it aligns the choices (choice-item elements) horizontally, otherwise vertically.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td> </td>
    <td> </td>
    <td> Used to specify ID value of the component.
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
    <td>If true, no selection causes validation error.
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
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Is the value attribute of the selected single choice-item element.
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
    <td>choice-item</td>
    <td> </td>
    <td> </td>
    <td>A child element of choice which indicates a single choice</td>
  </tr>
</table>


 

 

Attributes of the **_choice-item_** element:

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
This is similar to the class attribute in HTML elements.
 </td>
  </tr>
  <tr>
    <td>disabled</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the single choice is available.
If true, it can not accept user interactions and it will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to display as label of the single choice.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to select the single choice.
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
    <td>Is used as a multi-language key.
If set, the displayname attribute will be replaced by the corresponding value of the key in the multi-language resource.
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
    <td>selected</td>
    <td> </td>
    <td>false</td>
    <td>If true, the single choice is selected.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the single choice.
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
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Indicates the (internal) value of the single choice.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the single choice.
If false, the single choice is hidden.
 </td>
  </tr>
</table>


 

#### 6.14. Map

#### **Map**

Is an image with defined areas which can be clicked.

 

Tagname: **_map_**

 

Example:             

![image alt text](assets/images/image_6_10.png?raw=true)

 

              qaml code:

`<map name="planets" image="http://www.w3schools.com/tags/planets.gif">`

      `<area shape="rect" coords="0,0,82,126" alt="Sun" />`

      `<area shape="circle" coords="90,58,3" alt="Mercury" />`

      `<area shape="circle" coords="124,58,8" alt="Venus" />`

`</map>`

 

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
    <td>image</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the location of the image file.
 </td>
  </tr>
  <tr>
    <td>name</td>
    <td>*</td>
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
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>area</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Specifies an image with clickable areas by defining one or more area elements.</td>
  </tr>
</table>


 

 

Attributes of **_area_** element:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>alt</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the text to appear as hint of this area. When the area is being clicked it becomes the value of the Map component.
 </td>
  </tr>
  <tr>
    <td>coords</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the coordinates of the area.
The coordinates are depending on the shape attribute:
-                    rect: coords="x1,y1,x2,y2”
(top, left, bottom and right of the rectangle)
-                    circle: coords=”x,y,r”
(center position and radius of the circle)
-                    poly:  coords=”x1,y1,x2,y2,x3,y3…”
(position of corners of the polygon)
-                    default: does not need any coordinates
 </td>
  </tr>
  <tr>
    <td>shape</td>
    <td>*</td>
    <td> </td>
    <td>Specifies a shape for the area.
The possible values are:
-                    rect: a rectangular shape
-                    circle: a circular shape
-                    poly:  an arbitrary polygon, with 3 or more points
-                    default: which represents the remaining area of the image not defined by any area elements
 </td>
  </tr>
</table>


 

 

#### 6.15. Listbox

Displays a vertical list of items. The user can select one or more items from the list at the same time, specified by the *`multiple-selec*t` attribute.

It is composed of one or more *item* elements.

 

Tagname: **_listbox_**

Example:

              ![image alt text](assets/images/image_6_11.png?raw=true)

 

              qaml code:

`<listbox>`

         `<item` `displayname="List item 1"/>`

         `<item` `displayname="List item 2"/>`

	     `<item` `displayname="List item 3"/>`

`</listbox>`

 

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
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to edit the text of items.
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
    <td>multiple-select</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates one or more items can be selected at the same time.
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
    <td>nr-visible-items</td>
    <td> </td>
    <td> </td>
    <td>Specifies the number of items to be displayed. It should be a positive number.
 </td>
  </tr>
  <tr>
    <td>required</td>
    <td> </td>
    <td>false</td>
    <td>If true, at least one item must be selected, otherwise it causes a validation error.
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
    <td>item</td>
    <td> </td>
    <td> </td>
    <td>Element (see Attributes of item element).
Compose a list by defining one or more item elements.</td>
  </tr>
</table>


#### 6.16. Menu-definition

Defines a horizontal, top-level menu that contains one or more submenu items.

It is composed of one or more *menu *or* separator* elements.

This is defined outside the Window component, so it can be reused within the application context by assigning its ID to the *menu* or *contextmenu* attributes of some components.

 

Tagname: **_menu-definition_**

**_ _**

Example:

![image alt text](assets/images/image_6_12.png?raw=true)

 

qaml code:

`<window id="myWindow" displayname="My Window">`

      `<rootpanel menu="myMenu">`

            `<horizontallayout>`

            `</horizontallayout>`

      `</rootpanel>`

`</window>`

`<menu-definition id="myMenu">`

      `<menu id="menu1" displayname="Menu1">`

            `<menu id="menu1A" displayname="MenuItem 1-A" />`

      `</menu>`

      `<menu id="menu2" displayname="Menu2">`

            `<menu id="menu2A" displayname="MenuItem 2-A" />`

            `<separator />`

            `<menu id="menu2B" displayname="MenuItem 2-B">`

                  `<menu id="menu2B1" displayname="SubMenuItem 3-A" />`

                  `<menu id="menu2B2" displayname="SubMenuItem 3-B" />`

            `</menu>`

      `</menu>`

`</menu-definition>`

 

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
    <td>Text to display as menu item label.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td>*</td>
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
    <td>shortcut</td>
    <td> </td>
    <td> </td>
    <td>Is used for assigning a shortcut key for easy access.
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
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>menu</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Specifies submenu items which have the same attributes as the Menu-Definition component.</td>
  </tr>
  <tr>
    <td>separator</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
Indicates a horizontal line between two menu items.</td>
  </tr>
</table>


#### 6.17. Toolbar

#### **Toolbar-Definition**

Defines a horizontal group of logically related buttons with a common look and feel. It is composed of one or more *tb-item* elements. This is defined outside the Window component, so  that it can be reused within the application context by assigning its ID to the *toolbar* attributes of other components.

 

Tagname: **_toolbar-definition_**

** **

Example:

**              **![image alt text](assets/images/image_6_13.png?raw=true)

** **

              qaml code:

             

`<window id="myWindow" displayname="Toolbar">`

      `<rootpanel toolbar="myToolbar">`

            `<verticallayout>`

            `</verticallayout>`

      `</rootpanel>`

`</window>`

`<toolbar-definition id="myToolbar" item-width="20px" item-height="20px">`

      `<tb-item id="accept" image="accept.gif" tooltip="Accept" />`

      `<tb-item id="print" image=" print.gif" tooltip="Print" />`

      `<tb-item id="add" image="insert.gif" tooltip="Add Record" />`

      `<tb-item id="delete" image="delete.gif" tooltip="Delete Record" />`

`</toolbar-definition>`

** **

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
    <td>id</td>
    <td>*</td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>item-height</td>
    <td> </td>
    <td>16px</td>
    <td>Specifies the height of each toolbar item.
 </td>
  </tr>
  <tr>
    <td>item-width</td>
    <td> </td>
    <td>16px</td>
    <td>Specifies the width of each toolbar item.
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
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>tb-item</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Compose the toolbar by defining one or more tb-item elements.</td>
  </tr>
</table>


 

Attributes of **_tb-item_** element:

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
    <td>id</td>
    <td>*</td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>image</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the image location of the toolbar item.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the toolbar item.
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
</table>


#### 6.18. HTML

#### **HTML**

Is used to display HTML content by defining the *text* element.

 

Tagname: **_html_**

 

Example:

![image alt text](assets/images/image_6_14.png?raw=true)

 

qaml code:

	             `<html` `escape="true"` `width="300">`

           	             `<text><![CDATA[<button  displayname="Simple Button" />]]></text>`

              `</html>`

 

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
    <td>escape</td>
    <td> </td>
    <td>false</td>
    <td>If true, escapes the characters in a text.
 
For example: "bread" & "butter" becomes
"bread" & "butter"
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
    <td>preformat</td>
    <td> </td>
    <td>false</td>
    <td>If true, displays the text as it is.
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
    <td>text</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
HTML formatted text can be specified within this element.</td>
  </tr>
</table>


 

#### 6.19. Image

Lets you display image files, like JPG, PNG or GIF, at runtime, by defining the *location* attribute.

 

Tagname: **_image_**

 

Example:

![image alt text](assets/images/image_6_15.png?raw=true)

 

qaml code:

`<image` `location="http://www.google.com/intl/en_ALL/images/logo.gif"`

              `tooltip="This is an external image"/>`

 

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
    <td>location</td>
    <td> </td>
    <td> </td>
    <td>Specifies the location of the image file.
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


 

 

 

#### 6.20. Hidden

Is an invisible component for storing hidden values.

 

Tagname: **_hidden_**

 

Example:             

              [You will not see this component (!) ]

 

              qaml code:

              `<hidden` `value="value hidden"/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
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
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Specifies the hidden value.
 </td>
  </tr>
</table>


#### 6.21. Frame

Is used to show (external) web pages by defining the *src* attribute.

 

Tagname: **_frame_**

 

Example:

              ![image alt text](assets/images/image_6_16.png?raw=true)

 

              qaml code:

`<frame` `src="http://www.google.com"/>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
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
    <td>src</td>
    <td>*</td>
    <td> </td>
    <td>Indicates the URL.
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


 

#### 6.22. FileUpload

Lets the user upload a file to the server for processing.

 

Tagname: **_fileupload_**

 

Example:

![image alt text](assets/images/image_6_17.png?raw=true)

 

qaml code:

`<fileupload` `id="fileuploadId"` `editable="false"/>`

 

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
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to type text.
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


 

Referencing the id of the fileupload component will fetch a Map object containing the byte array of the file content, the name of the file and the mime-type. In the desired service class to which the Map object is passed, use the key *filecontent, filename *and *mime-type *to get respective data from related to the uploaded file.

#### 6.23. Panel

Contains one or more child components (aka container). Therefore, it must have a layout to align its children.

 

It can have the following layout elements:

-         *horizontallayout*

-         *verticallayout*

-         *gridlayout*

-         *borderlayout*

-         *absolutelayout*

-         *autolayout*

 

Tagname: **_panel_**

**_ _**

Example:

![image alt text](assets/images/image_6_18.png?raw=true)

 

qaml code:

`<label displayname="This is a Horizontal Panel" />`

`<panel>`

      `<horizontallayout>`

            `<button displayname="1" width="30px" />`

            `<button displayname="2" width="30px" />`

            `<button displayname="3" width="30px" />`

      `</horizontallayout>`

`</panel>`

 

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
If true, it can not accept user interactions and the component will be grayed out. The child components will also have the same state as its parent component.
 </td>
  </tr>
  <tr>
    <td>disclosure</td>
    <td> </td>
    <td>false</td>
    <td>If true, a triangle shape will appear on the left top side of the component. Clicking on the triangle will expand or collapse the content.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Specifies the text as title of the panel.
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
    <td>Is used for data mapping or grouping of components. When name attribute of a panel is used as reference, then components in the panel with name attributes are fetched. Its advised to use different value for name and id of components.
This attribute of a panel can also be used to fetch individual values of components with name attribute. 
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
    <td>toolbar</td>
    <td> </td>
    <td> </td>
    <td>Specifies the toolbar associated with this component. Positioned on the top of the panel.
It refers to a toolbar which is defined as a toolbar-definition.
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
If false, the component is hidden. The child components will also have the same state as its parent component.
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


 

##### 6.24. Layout elements

** **

###### 6.24.1. horizontallayout

Lays out components in a single horizontal row.

No attributes.

 

Example:

`<panel>`

`<horizontallayout>`

`<button/>`

`<button/>`

`  </horizontallayout>`

`</panel>`

** **

** **

###### 6.24.2. verticallayout

Lays out components in a single vertical column.

No attributes.

 

Example:

`<panel>`

`<verticallayout>`

`<button/>`

`<button/>`

`</verticallayout>`

`</panel>`

**_ _**

**_ _**

###### 6.24.3. gridlayout

Arranges components as rows and columns.

 

Example:

`<panel>`

`<gridlayout>`

`<element` `x="0"` `y="0">`

 	          	             `<label/>`

 	             `</element>`

 	             `<element` `x="1"` `y="0">`

   	             `<textfield/>`

 	             `</element>`

                `</gridlayout>`

`</panel>`             

** **

Attributes of **_element_** element:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>gridheight</td>
    <td> </td>
    <td> </td>
    <td>Number of rows spanned by the cell.
 </td>
  </tr>
  <tr>
    <td>gridwidth</td>
    <td> </td>
    <td> </td>
    <td>Number of columns spanned by the cell.
 </td>
  </tr>
  <tr>
    <td>x</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the column of the cell.
 </td>
  </tr>
  <tr>
    <td>y</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the row of the cell.
 </td>
  </tr>
</table>


** **

** **

###### 6.24.4. borderlayout

Arranges components to the five regions: north, south, east, west, and center.

 

Example:

`<panel>`

      `<borderlayout>`

            `<north>`

                  `<label />`

            `</north>`

            `<east>`

                  `<label />`

            `</east>`

            `<south>`

                  `<label />`

            `</south>`

            `<west>`

                  `<label />`

            `</west>`

            `<center>`

                  `<label />`

            `</center>`

      `</borderlayout>`

`</panel>`

            

** **

** **

###### 6.24.5. absolutelayout

Lets you specify the position of components using the *x* and *y* attributes of each *element* element.

 

Example:

`<panel>`

                `<absolutelayout>`

 	          	             `<element` `x="10"` `y="20">`

   	          	             `<label/>`

 	          	             `</element>`

 	          	             `<element` `x="180"` `y="350">`

   	          	             `<textfield/>`

 	          	             `</element>`

                `</absolutelayout>`

`</panel>`             

 

Attributes of **_element_** element:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>x
 </td>
    <td>*</td>
    <td> </td>
    <td>Specifies the x position of the element.
 </td>
  </tr>
  <tr>
    <td>y
 </td>
    <td>*</td>
    <td> </td>
    <td>Specifies the y position of the element.
 </td>
  </tr>
</table>


 

 

###### 6.24.6. autolayout

Lays out components in a multi vertical columns, specified by the *cols* attribute

 

Example:

`<panel>`

                `<autolayout cols="2">`

   	             `<label/>`

   	             `<textfield/>`

                `</autolayout>`

`</panel>`             

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>cols
 </td>
    <td> </td>
    <td>1</td>
    <td>Specifies the number of vertical columns to layout the child components.
 </td>
  </tr>
</table>


 

####  6.25. Panel definition

Is a reusable Panel component.

Setting the *id* attribute is mandatory, because it will be used as a reference by the Panel-Ref component. This component is defined outside the Window component, so it can be reused in other Window components. Therefore, the ID should be unique within an application context.

 

Example:

![image alt text](assets/images/image_6_19.png?raw=true)

 

              qaml code:

`<window` `id="myWindow"` `displayname="My Window">`

	     `<rootpanel>`             

           	  `<horizontallayout>`           	          	          	          	            

           	  		`<panel-ref` `id="myPanelRef"` `ref="myPanel"/>`

         		`</horizontallayout>`

 		`</rootpanel>`

 `</window>`

`<panel-definition` `id="myPanel">`

		`<horizontallayout>`

        		`<button` `displayname="1"` `width="30px"/>`

           	 `<button` `displayname="2"` `width="30px"/>`

           	 `<button` `displayname="3"` `width="30px"/>`

        `</horizontallayout>`

 `</panel-definition>`

#### 6.26. Panel ref

Refers to a container which is defined as a Panel-Definition component.

 

Example:

![image alt text](assets/images/image_6_20.png?raw=true)

 

              qaml code:

`<window id="myWindow" displayname="My Window">`

      `<rootpanel>`

            `<horizontallayout>`

                  `<panel-ref id="myPanelRef" ref="myPanel" />`

            `</horizontallayout>`

      `</rootpanel>`

`</window>`

`<panel-definition id="myPanel">`

      `<horizontallayout>`

            `<button displayname="1" width="30px" />`

            `<button displayname="2" width="30px" />`

            `<button displayname="3" width="30px" />`

      `</horizontallayout>`

`</panel-definition>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>id</td>
    <td>*</td>
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
    <td>ref</td>
    <td>*</td>
    <td> </td>
    <td>Refers to the ID of a Panel-Definition component.
 </td>
  </tr>
</table>


#### 6.27. Splitpanel

Lays out its 2 child containers horizontally by default. It inserts a draggable divider in the gap between the children. The user can drag the divider to resize the children on each side. The child containers are defined by the *first* and *second* elements.

 

Tagname: **_splitpanel_**

 

Example:

              ![image alt text](assets/images/image_6_21.png?raw=true)

 

qaml code:

`<splitpanel width="300" height="100" horizontal="true">`

      `<first>`

            `<panel displayname="Top">`

                  `<autolayout>`

                        `<label displayname="Top" />`

                  `</autolayout>`

            `</panel>`

      `</first>`

      `<second>`

            `<panel displayname="Bottom">`

                  `<autolayout>`

                        `<label displayname="Bottom" />`

                  `</autolayout>`

            `</panel>`

      `</second>`

`</splitpanel>`

 

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
If true, it can not accept user interactions and the component will be grayed out. The child components will also have the same state as its parent component.
 </td>
  </tr>
  <tr>
    <td>height</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the height of the component, usually in pixels.
 </td>
  </tr>
  <tr>
    <td>horizontal</td>
    <td> </td>
    <td>true</td>
    <td>If true, the first and second elements are laid out horizontally, otherwise vertically.
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
    <td>position</td>
    <td> </td>
    <td>50%</td>
    <td>If the horizontal attribute is set to true, it specifies the width of the first element, otherwise it specifies the height of the first element. If the unit is in percentage it will use the width or height attribute to determine the width or height of the first element.
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
    <td>*</td>
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
    <td>first</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
It contains one component.</td>
  </tr>
  <tr>
    <td>second</td>
    <td> </td>
    <td> </td>
    <td>Element which has no attributes.
It contains one component.</td>
  </tr>
</table>


           	       

#### 6.28. Stackpanel

Has a collection of child containers, but only one of them at a time is visible. It creates navigator buttons (*displayname* attribute of the *stack* element), which you use to navigate between the children. When the user clicks a navigator button, the associated child container is displayed.

 

Tagname: **_stackpanel_**

 

Example:

![image alt text](assets/images/image_6_22.png?raw=true)

 

              qaml code:

`<stackpanel>`

      `<stack displayname="Stack one">`

            `<button displayname="Stack one" />`

      `</stack>`

      `<stack displayname="Stack two">`

            `<label displayname="Stack two" />`

      `</stack>`

      `<stack displayname="Stack three">`

            `<checkbox displayname="Stack three" />`

      `</stack>`

`</stackpanel>`

 

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
    <td>stack</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Compose a collection by defining one or more stack elements. Each stack element contains one component.</td>
  </tr>
</table>


 

 

Attributes of **_stack_** element:

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
    <td>*</td>
    <td> </td>
    <td>Specifies the label of the navigator button, associated with the stack element.
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
    <td>Specifies the inline CSS style for the stack element.
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
</table>


 

 

#### 6.29. Tilelist

#### **Tilelist**

Displays a number of items laid out in tiles. An item can be any component. 

Tagname: **_tilelist_**

 

Example:

![image alt text](assets/images/image_6_23.png?raw=true)

             

qaml code:

`<tilelist id="scores" columns="1" width="410" height="610">`

      `<panel height="75">`

            `<gridlayout>`

                  `<element x="0" y="0">`

                        `<label displayname="Score" />`

                  `</element>`

                  `<element x="1" y="0">`

                        `<label name="score" />`

                  `</element>`

                  `<element x="0" y="1">`

                        `<label displayname="Name" />`

                  `</element>`

                  `<element x="1" y="1">`

                        `<label name="name" />`

                  `</element>`

                  `<element x="0" y="2">`

                        `<label displayname="Email" />`

                  `</element>`

                  `<element x="1" y="2">`

                        `<label name="email" />`

                  `</element>`

                  `<element x="2" y="2">`

                        `<label displayname="Phone number" />`

                  `</element>`

                  `<element x="3" y="2">`

                        `<label name="phone" />`

                  `</element>`

            `</gridlayout>`

      `</panel>`

`</tilelist>`

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
    <td>columns</td>
    <td> </td>
    <td>1</td>
    <td>Specifies the number of columns to layout the tiles horizontally.
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


 

 

 

#### 6.30. Table

#### **Table**

Contains a header and one or more rows which can have multiple columns. It is used for static content.

 

Tagname: **_table_**

 

Example:

![image alt text](assets/images/image_6_24.png?raw=true)

             

qaml code:

`<table>`

      `<header>`

            `<cell>`

                  `<label displayname="header 1" />`

            `</cell>`

            `<cell>`

                  `<label displayname="header 2" />`

            `</cell>`

      `</header>`

      `<row>`

            `<cell>`

                  `<button displayname="button row 1" />`

            `</cell>`

            `<cell>`

                  `<button displayname="second button row 1" />`

            `</cell>`

      `</row>`

      `<row>`

            `<cell>`

                  `<button displayname="button row 2" />`

            `</cell>`

            `<cell>`

                  `<button displayname="second button row 2" />`

            `</cell>`

      `</row>`

`</table>`

 

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
    <td>header</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
It contains one or more cell elements, indicate as header columns.</td>
  </tr>
  <tr>
    <td>row</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Compose a table with content by defining one or more row elements. Each row element contains one or more cell elements, indicate as row columns.</td>
  </tr>
</table>


 

           	          	          	            

Attributes of **_header_** element:

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
    <td>Indicates whether the header is available.
If true, it can not accept user interactions and the header will be grayed out.
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
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the header element.
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
    <td>Indicates the visibility of the header.
If false, the header is hidden.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>cell</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
It contains one component.</td>
  </tr>
</table>


           	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	          	            

Attributes of **_row_** element:

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
    <td>Indicates whether the row is available.
If true, it can not accept user interactions and the row will be grayed out.
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
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the row element.
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
    <td>True</td>
    <td>Indicates the visibility of the row.
If false, the row is hidden.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>cell</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
It contains one component.</td>
  </tr>
</table>


           	          	          	            

 

Attributes of **_cell_** element:

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
    <td>False</td>
    <td>Indicates whether the cell is available.
If true, it can not accept user interactions and the cell will be grayed out.
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
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the cell element.
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
    <td>True</td>
    <td>Indicates the visibility of the cell.
If false, the cell is hidden.
 </td>
  </tr>
</table>


 

#### 6.31. TabPanel

Lets you create a horizontal group of tab navigation items. It is composed of one or more Panel components, indicated as tab elements.

 

Tagname: **_tabpanel_**

**_ _**

Example:

![image alt text](assets/images/image_6_25.png?raw=true)

             

qaml code:

             

`<tabpanel>`

      `<tab displayname="Example">`

            `<verticallayout>`

                  `<button displayname="Simple Button" />`

            `</verticallayout>`

      `</tab>`

      `<tab displayname="Source code">`

            `<verticallayout>`

                  `<html height="100%" width="100%" escape="true">`

	                  `<text><![CDATA[<button  displayname="Simple Button"/>]]></text>`

                  `</html>`

            `</verticallayout>`

      `</tab>`

`</tabpanel>`

 

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
    <td>tab</td>
    <td> </td>
    <td> </td>
    <td>Element which has the same attributes as the Panel component.
Indicates as a Panel component.</td>
  </tr>
</table>


           	            

#### 6.32. Tree

#### **Tree**

Lets the user view hierarchical data arranged as an expandable tree.

Each item in a tree is a *tree-item* element which also can contain other *tree-item* elements.

 

Tagname: **_tree_**

**_ _**

Example:

              ![image alt text](assets/images/image_6_26.png?raw=true)

 

              qaml code:

             

`<tree displayname="My Tree" id="myTree" width="150">`

      `<tree-item displayname="Buttons">`

            `<tree-item id="simpleButton" displayname="Simple Button" />`

      `</tree-item>`

      `<tree-item displayname="Imaging">`

            `<tree-item id="image" displayname="Image" />`

            `<tree-item id="map" displayname="Map" />`

      `</tree-item>`

`</tree>`

 

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
    <td>Text to display as tree item label.
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
    <td>tree-item</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
Compose a tree by defining one or more tree-item elements which also have sub tree-item elements.</td>
  </tr>
</table>


 

 

Attributes of **_tree-item_** element:

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
    <td>Indicates whether the tree item is available.
If true, it can not accept user interactions and the component will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to display as tree item label.
 </td>
  </tr>
  <tr>
    <td>expand</td>
    <td> </td>
    <td>false</td>
    <td>Indicates the state of the tree item. If true, the sub tree items will be shown.
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
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the tree item.
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
    <td>value</td>
    <td> </td>
    <td> </td>
    <td>Specifies the (internal) value of the tree item.
 </td>
  </tr>
  <tr>
    <td>visible</td>
    <td> </td>
    <td>true</td>
    <td>Indicates the visibility of the tree item.
If false, the tree item is hidden.
 </td>
  </tr>
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>tree-item</td>
    <td> </td>
    <td> </td>
    <td>Element which has the same attributes as the tree-item element. Compose sub tree items by defining one or more tree-item elements.</td>
  </tr>
</table>


 

#### 6.33. Window

#### **Window**

Is a top-level container for holding components. A window is required to have a rootpanel element for which a layout element must be specified.

 

Tagname: **_window_**

**_ _**

Example:

![image alt text](assets/images/image_6_27.png?raw=true)

                           

qaml code:

`<window id="myWindow" displayname="My Window">`

      `<rootpanel>`

            `<horizontallayout>`

                  `<textfield id="name" type="text" displayname="Name" />`

            `</horizontallayout>`

      `</roottabpanel>`

`</window>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>authentication-required</td>
    <td> </td>
    <td>false</td>
    <td>If true, a specified login window will be shown first for authentication before opening this window. If succeeded, this window will be opened afterward.
 </td>
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
    <td>closeable</td>
    <td> </td>
    <td>true</td>
    <td>If false, the close button on the top right of the window is not visible.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td>*</td>
    <td> </td>
    <td>Specifies the title of the window.
 </td>
  </tr>
  <tr>
    <td>draggable</td>
    <td> </td>
    <td>true</td>
    <td>If false, the window can not be moved.
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
    <td>icon</td>
    <td> </td>
    <td> </td>
    <td>Specifies the location of the icon. The icon will appear on the "desktop" or “dock”, specified by the in-dock attribute.
 </td>
  </tr>
  <tr>
    <td>icon-style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style of the icon attribute.
 </td>
  </tr>
  <tr>
    <td>id</td>
    <td>*</td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>in-dock</td>
    <td> </td>
    <td>false</td>
    <td>If true, the specified icon attribute will be placed in the “dock”, instead of “desktop”.
 </td>
  </tr>
  <tr>
    <td>isparent</td>
    <td> </td>
    <td>true</td>
    <td>If false, the window is not visible in the system menu, so it can not be opened by user interactions.
 </td>
  </tr>
  <tr>
    <td>left</td>
    <td> </td>
    <td> </td>
    <td>Specifies the horizontal position of the window within the entire application.
 </td>
  </tr>
  <tr>
    <td>maximizable</td>
    <td> </td>
    <td>true</td>
    <td>If false, the maximize button on the top right of the window is not visible.
 </td>
  </tr>
  <tr>
    <td>message-key</td>
    <td> </td>
    <td> </td>
    <td>Is used for multi-language.
If set, the displayname attribute will be replaced by the multi-language resource.
???</td>
  </tr>
  <tr>
    <td>minimizable</td>
    <td> </td>
    <td>true</td>
    <td>If false, the minimize button on the top right of the window is not visible.
 </td>
  </tr>
  <tr>
    <td>resizable</td>
    <td> </td>
    <td>true</td>
    <td>If false, the size of the window can not be changed.
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
    <td>top</td>
    <td> </td>
    <td> </td>
    <td>Specifies the vertical position of the window within the entire application.
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
    <td>rootpanel</td>
    <td>*</td>
    <td> </td>
    <td>Element.
Indicates the top level Panel component.</td>
  </tr>
  <tr>
    <td>events</td>
    <td> </td>
    <td> </td>
    <td>Element.
Define events to handle user interactions.</td>
  </tr>
  <tr>
    <td>styles</td>
    <td> </td>
    <td> </td>
    <td>Element.
Specify the external cascading style sheet for the window.</td>
  </tr>
</table>


 

           	          	          	            

           	          	          	            

 

 

#### 6.33. Datagrid

#### **Datagrid**

Is a table like structure suitable for showing lists of objects with multiple properties. The datagrid element houses *column *elements.

 

Tagname: **_datagrid_**

 

Example:

              ![image alt text](assets/images/image_6_28.png?raw=true)

 

Qaml code:

`<datagrid` `id="myDatagrid"` `name="Persons">`

`<column` `id="lastname"` `name="lastname" displayname="lastname"/>`

             `<column` `id="age"` `name="age" displayname ="age"/>`

`</datagrid>`

 

Attributes:

<table>
  <tr>
    <td>Name</td>
    <td>Req</td>
    <td>Default</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>add</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates that an internal add control button will appear below the Datagrid component.

For having the functionality of add effected an onclick listener should be used which listens to <datagridId>.add


The event for the internal add control button will look as follows

<event>
   <listeners>
      <listenergroup>
	   <component ref="datagridID.add"/>	              
   	      <listener type="onclick"/>
      </listenergroup>
   </listeners>
</event>

This control button can be customized by defining the controlbar element and can specify your own customized add button in it.
 
This attribute will be ignored when the controlbar element is specified.
 </td>
  </tr>
  <tr>
    <td>class</td>
    <td> </td>
    <td> </td>
    <td>Refers to the CSS style class from an external CSS file.
This is similar to the class attribute in HTML elements.

Setting the style for this class applies to the datagrid as a whole and all of its subcomponents. 
For specifying styles on components within the datagrid, there are some predefined classes which can be applied on top of the class itself.

Subclass 'headerWrapper' is used for defining the style of the header row.
Subclass 'dataTable' is used for defining the style of the rows.

Within subclass 'dataTable' style selectors can be specified to have a style for selecting or hover table rows.

'td.highlighted' is applied when hovering over a cell.
'tr.highlighted' is applied when hovering over a row.
'tr.selected' is applied when selecting a row.

Example :


<datagrid id="myDatagrid" name="Persons" class="myDatagridStyleClass"/>

can be styled with desired attributes mentioned in style classes defined as follows in a stylesheet :

.myDatagridStyleClass {}
.myDatagridStyleClass .headerWrapper {}
.myDatagridStyleClass .dataTable {}
.myDatagridStyleClass .dataTable td.highlighted {}
.myDatagridStyleClass .dataTable tr.highlighted {}
.myDatagridStyleClass .dataTable tr.selected {}

</td>
  </tr>
  <tr>
    <td>currentpage</td>
    <td> </td>
    <td>0</td>
    <td>Indicates the current page when paging is enabled.
Is used when the pagesize attribute is set.
 </td>
  </tr>
  <tr>
    <td>delete</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates that an internal delete control button will appear below the Datagrid component.


For having the functionality of delete effected an onclick listener should be used which listens to <datagridId>.delete


The event for the internal delete control button will look as follows

<event>
   <listeners>
      <listenergroup>
	   <component ref="datagridID.delete"/>	              
   	      <listener type="onclick"/>
      </listenergroup>
   </listeners>
</event>
 

Clicking on the delete control button will remove selected rows from the datagrid.
 
See also the add attribute.
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
    <td>editable</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the user is allowed to edit cells.
 </td>
  </tr>
  <tr>
    <td>export</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates that an internal export control button will appear below the Datagrid component.
 
See also the add attribute.
 </td>
  </tr>
  <tr>
    <td>export-formats</td>
    <td></td>
    <td>excel,pdf,csv,xml</td>
    <td>When export=true, user can specify the desired formats comma separated.
Supported formats : excel,pdf,csv,xml</td>
  </tr>
  <tr>
    <td>group-name</td>
    <td></td>
    <td></td>
    <td>Used to specify group-name for the component. Multiple setgroup names can be mentioned separated by comma. In case of datagrid, if group-names are mentioned in column definitions, then when referring filtering happens based on the referred group name such that the data returned will have only those columns which has the matching group name. The group names mentioned for the column should also be specified in the datagrid for this to work.</td>
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
    <td>minrows</td>
    <td> </td>
    <td>5</td>
    <td>Indicates the minimum number of rows to display.
 </td>
  </tr>
  <tr>
    <td>multiple-select</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates one or more rows can be selected at the same time.
 </td>
  </tr>
  <tr>
    <td>row-colors</td>
    <td></td>
    <td></td>
    <td>color codes as per CSS standard can be specified as value separated by comma to this attribute in order to have alternating row colors on a datagrid. The values specified in this attribute will override other style classes affecting the row.</td>
  </tr>
  <tr>
    <td>name</td>
    <td> </td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>pagesize</td>
    <td> </td>
    <td>-1</td>
    <td>A set value indicates that paging is enabled. The set value specifies the number of records to fetch each time. Navigation control (built-in) buttons (first, previous, next and last) will appear if the controlbar element is not defined. For having the functionality of paging an onclick listener should be used which listens to <datagridId>.firstPage, <datagridId>.previousPage, <datagridId>.nextPage, <datagridId>.lastPage. The internal variable $OFFSET represents the actual current page.

The event for paging will look as follows
<event>
   <listeners>
      <listenergroup>
	   	  <component ref="datagrid1ID.firstPage"/>        	     	   
      	   <component ref="datagrid1ID.previousPage"/>
	   <component ref="datagrid1ID.nextPage"/>
	   <component ref="datagrid1ID.lastPage"/>   	           
   	      <listener type="onclick"/>
      </listenergroup>
   </listeners>

  <business-action ref="getData">
	<out name="result" ref="result"/>
  </business-action>
  <set component-id="datagridID" ref="result"/>

   <set-property property="currentpage" ref="$OFFSET">
      <component ref="datagrid1ID"/>
   </set-property>
</event>
 
In order to have the paging property when the datagrid is rendered for first time  following must be included before setting data.


<store name="$PAGESIZE" src="component" ref="mydatagrid3@pagesize"/>

<store name="$OFFSET" value="0"/>   

The scrollable argument for the method which fetches data for the datagrid should be set to true

</td>
  </tr>
  <tr>
    <td>page-scroll</td>
    <td></td>
    <td>false</td>
    <td>Specifies endless scrolling is enabled or not. 

To make it enabled you have to set page-size greater than 0  value and 'scrollable' attribute of the method used to fetch data should be set as 'true'.
If page-scroll is set as 'true' normal paging options will not be available.

<datagrid id="dbDatagrid3" name="dbDatagrid3" pagesize="8" page-scroll="true"/> 
...
<event>
	<listeners>
		<listenergroup>
			<component ref="dbDatagrid3"/>
			<listener type="onscroll-bottom"/>
		</listenergroup>
	</listeners>
	<business-action ref="populateDatagridFromDB">
	<out name="dbData" ref="resultFromDBBA"/>
	</business-action>
	<set component-id="dbDatagrid3" ref="dbData" 	action="add"/>
</event></td>
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
    <td>column</td>
    <td> </td>
    <td> </td>
    <td>Element which has attributes.
A component can be defined within this element to have different appearance, like a Checkbox component when the value is true or false. Or a Date component when the value is date.</td>
  </tr>
  <tr>
    <td>overflow</td>
    <td> </td>
    <td> </td>
    <td>An element which has the same attributes as the Panel component. An overflow is a panel inside the datagrid component which is displayed below the datagrid (not appearing as columns). Within the overflow element more details can be shown by adding extra fields.</td>
  </tr>
  <tr>
    <td>controlbar</td>
    <td> </td>
    <td> </td>
    <td>An element which has attributes on it's own and also attributes from the Panel component.
It is a panel where you can add customized control buttons. It will ignore the built-in control buttons like add, delete, export and navigation (when defined).</td>
  </tr>
</table>


 

As per the values of the attributes - add, delete or editable, an extra column representing row number and a toolbar as shown below will appear along with the datagrid.

![image alt text](assets/images/image_6_29.png?raw=true)

Associated to each button on the toolbar changes will be reflected to the data in the datagrid. Clicking on add button of the toolbar will provide an empty row at the end of the datagrid with '+' symbol along with the row number. When rows are selected and opted for deletion, a '-' symbol and when existing data is modified a '*' symbol will appear along with the row number.

Keywords:

<table>
  <tr>
    <td>reference</td>
    <td>description</td>
  </tr>
  <tr>
    <td>datagridId</td>
    <td>returns selected rows</td>
  </tr>
  <tr>
    <td>datagridId.$$NEW</td>
    <td>returns new rows</td>
  </tr>
  <tr>
    <td>datagridId.$$DELETED</td>
    <td>returns deleted rows</td>
  </tr>
  <tr>
    <td>datagridId.$$MODIFIED</td>
    <td>returns modified rows</td>
  </tr>
  <tr>
    <td>datagridId.$$UNSELECTED</td>
    <td>returns all rows except selected rows</td>
  </tr>
  <tr>
    <td>datagridId.$$ALL</td>
    <td>returns all rows</td>
  </tr>
  <tr>
    <td>datagridId.rowNumber</td>
    <td>uses in an event for defining listener types for the internal rowNumber column</td>
  </tr>
</table>


The cancel button on the toolbar will re-initialize the datagrid with the last saved state. If needed, Business logic for refresh button action needs to be specified by the QAML developer.

A QAML developer can choose to do operations based on the toolbar button actions by having events with onclick listener on datagridId.add, datagridId.delete, datagridId.save, datagridId.refresh and/or datagridId.cancel which can be used as referencing component ids in an event.

Attributes of **_column_** element:

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
    <td>content</td>
    <td> </td>
    <td>string</td>
    <td>Indicates the appearance of the content available from the object property.
The possible values are:
-         string: render as "label"
-         html: render HTML formatted text as HTML page
-         checkbox: render as Checkbox component, based on the value (true or false) the check mark is set or not set
-         link: render as “hyperlink”, clicking on the link the displaying text is used as value
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
    <td>Text to display as the column header.
 </td>
  </tr>
  <tr>
    <td>editable</td>
    <td> </td>
    <td>true</td>
    <td>Indicates whether the user is allowed to edit the column.
 </td>
  </tr>
  <tr>
    <td>group-name</td>
    <td></td>
    <td></td>
    <td>Used to specify group names so that when datagrid is referred using group name filtering happens. The group name mentioned for columns should also be included in the group name for the datagrid.</td>
  </tr>
  <tr>
    <td>height</td>
    <td> </td>
    <td> </td>
    <td>Specifies the height of the column, usually in pixels.
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
    <td>Is used as a multi-language key.
If set, the displayname attribute will be replaced by the corresponding value of the key in the multi-language resource.
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
    <td>sortable</td>
    <td> </td>
    <td>false</td>
    <td>Indicates whether the column can be sorted when clicking on the column header. If this attribute is made true, the associated event onfetchdata must be implemented followed by the business action to fill the datagrid with data in order to have the functionality.
 </td>
  </tr>
  <tr>
    <td>static</td>
    <td> </td>
    <td>false</td>
    <td>If true, indicates that the column is not mapped to any data, so the content is static or it contains a component, like a button or image.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the column.
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
    <td>Indicates the visibility of the column.
If false, the column is hidden.
 </td>
  </tr>
  <tr>
    <td>width</td>
    <td> </td>
    <td> </td>
    <td>Specifies the width of the column, usually in pixels.</td>
  </tr>
</table>


 

 

Attributes of **_controlbar_** element:

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
    <td>placement</td>
    <td> </td>
    <td>bottom</td>
    <td>Specifies the position of this panel with respect to the Datagrid component.
The possible values are:
-         top: place above the Datagrid component, layout of the panel should be horizontal
-         left: place on the left side of the Datagrid component, layout of the panel should be vertical
-         bottom: place below the Datagrid component, layout of the panel should be horizontal
-         right: place on the right side of the Datagrid component, layout of the panel should be vertical
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the controlbar.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
</table>


             

Setting and getting cell values on a datagrid component:

A qaml developer can use the available syntax mentioned below in order to set or get a cell value with respect to a row in a datagrid component.

**By Specifying row number directly:- **(Row index starts from 0)

To set: **<****set**** ****component-id****=****_"myDatagridId[<ROW>].<COLUMN NAME>"_**** …./>**

To Get: **<****_<BUILT IN>_**** ****ref****=****_"myDataGrid[<ROW>].<COLUMN NAME>"_**** ****src****=****_"component"_****/>**

**By Specifying set/get on selected row:-**

To set: **<****set**** ****component-id****=****_"myDatagridId[_****_$SELECTED_INDEX_****_].<COLUMN NAME>"_**** …./>**

To Get:**<****_<BUILT IN>_**** ****ref****=****_"myDataGrid[_****_$SELECTED_INDEX_****_].<COLUMN NAME>"_**** ****src****=****_"component"_****/>**

#### Drop down as inner component for a column in a datagrid:

It is possible to manually define components inside a column definition for a datagrid. 

When using drop down component as an inner component, qaml developer must make sure that the drop down component is set first, dynamically or statically, before setting the datagrid.

In such scenarios the column where the dropdown inner component is defined must have an id and that id along with datagrid’s id is used to set value to the dropdown component.

<set component-id=*"<DATAGRID ID>.<COLUMN ID>"* …./>

### 6.34. Charting support

#### 6.34.1. BarChart

The BarChart component represents data as items of horizontal bars.

 

Tagname: **_barchart_**

 

Example:

              ![image alt text](assets/images/image_6_30.png?raw=true)

 

<table>
  <tr>
    <td>month</td>
    <td>profit</td>
    <td>expenses</td>
  </tr>
  <tr>
    <td>Jan</td>
    <td>2000</td>
    <td>1500</td>
  </tr>
  <tr>
    <td>Feb</td>
    <td>1000</td>
    <td>200</td>
  </tr>
  <tr>
    <td>Mar</td>
    <td>1500</td>
    <td>500</td>
  </tr>
  <tr>
    <td>Apr</td>
    <td>1800</td>
    <td>1200</td>
  </tr>
  <tr>
    <td>May</td>
    <td>2400</td>
    <td>575</td>
  </tr>
</table>


qaml code:

`<barchart legend="none">`

      `<category-axis name="month" />`

      `<chart-item displayname="Profit" name="profit" />`

      `<chart-item displayname="Expenses" name="expenses" />`

`</barchart>`

 

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
    <td>Text to appear as title.
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
    <td>legend</td>
    <td> </td>
    <td>right</td>
    <td>Specifies the position of the legend with respect to the chart component.
The possible values are:
-         top: place above the chart component, lays out horizontally
-         left: place on the left side of the chart component, lays out vertically
-         bottom: place below chart component, lays out horizontally
-         right: place on the right side of the chart component, lays out vertically
-         none: no legend
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
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>category-axis</td>
    <td>1</td>
    <td> </td>
    <td>Element which has attributes.
Lets a chart represent data grouped by a set of values along an axis. It represents a vertical axis of the BarChart component.</td>
  </tr>
  <tr>
    <td>linear-axis</td>
    <td>0..1</td>
    <td> </td>
    <td>Element which has attributes.
Maps numeric values evenly between a minimum and maximum value along an axis. It represents a horizontal axis of the BarChart component.</td>
  </tr>
  <tr>
    <td>chart-item</td>
    <td>1..N</td>
    <td> </td>
    <td>Element which has attributes.
Specifies a chart item for a chart component.</td>
  </tr>
</table>


 

Attributes of **_category-axis_** element:

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
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Indicates the label of the axis.
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
    <td>*</td>
    <td> </td>
    <td>Is used for data mapping or grouping of components.
 </td>
  </tr>
  <tr>
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the header element.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
</table>


           	          	          	          	          	          	          	          	          	          	          	          	            

 

Attributes of **_linear-axis_** element:

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
    <td>id</td>
    <td> </td>
    <td> </td>
    <td>Used to specify ID value of the component.
The ID should be unique within a Window component.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Indicates the label of the axis.
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
    <td>max-value</td>
    <td> </td>
    <td> </td>
    <td>Specifies the maximum value for this axis.
Applicable to number values.
 </td>
  </tr>
  <tr>
    <td>min-value</td>
    <td> </td>
    <td> </td>
    <td>Specifies the minimum value for this axis.
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
    <td>style</td>
    <td> </td>
    <td> </td>
    <td>Specifies the inline CSS style for the header element.
This is similar to the style attribute in HTML elements.
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camelcase).
 
Multiple style properties can be added, as long as they are separated by the semi-colon (;).
 </td>
  </tr>
  <tr>
    <td>ticksize</td>
    <td> </td>
    <td> </td>
    <td>The spacing between label values along this axis.
 </td>
  </tr>
</table>


#### ** **

Attributes of **_chart-item_** element:

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
    <td>Indicates whether the chart item is available.
If true, it can not accept user interactions and the chart item will be grayed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Indicates the name of the chart item, for displaying to the user.
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
    <td>*</td>
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
    <td>Indicates the visibility of the chart item.
If false, the chart item is hidden.
 </td>
  </tr>
</table>


#### 6.34.2. ColumnChart

The ColumnChart component represents data as items of vertical bars.

 

Tagname: **_columnchart_**

 

Example:

<table>
  <tr>
    <td>month</td>
    <td>profit</td>
    <td>expenses</td>
  </tr>
  <tr>
    <td>Jan</td>
    <td>2000</td>
    <td>1500</td>
  </tr>
  <tr>
    <td>Feb</td>
    <td>1000</td>
    <td>200</td>
  </tr>
  <tr>
    <td>Mar</td>
    <td>1500</td>
    <td>500</td>
  </tr>
  <tr>
    <td>Apr</td>
    <td>1800</td>
    <td>1200</td>
  </tr>
  <tr>
    <td>May</td>
    <td>2400</td>
    <td>575</td>
  </tr>
</table>


![image alt text](assets/images/image_6_31.png?raw=true)                           

 

 qaml code:

`<columnchart legend="left">`

      `<category-axis name="month" />`

      `<chart-item displayname="Profit" name="profit" />`

      `<chart-item displayname="Expenses" name="expenses" />`

`</columnchart>`

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
    <td>Text to appear as title.
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
    <td>legend</td>
    <td> </td>
    <td>right</td>
    <td>Specifies the position of the legend with respect to the chart component.
The possible values are:
-         top: place above the chart component, lays out horizontally
-         left: place on the left side of the chart component, lays out vertically
-         bottom: place below chart component, lays out horizontally
-         right: place on the right side of the chart component, lays out vertically
-         none: no legend
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
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>category-axis</td>
    <td>1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Lets a chart represent data grouped by a set of values along an axis. It represents a horizontal axis of the ColumnChart component.</td>
  </tr>
  <tr>
    <td>linear-axis</td>
    <td>0..1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Maps numeric values evenly between a minimum and maximum value along an axis. It represents a vertical axis of the ColumnChart component.</td>
  </tr>
  <tr>
    <td>chart-item</td>
    <td>1..N</td>
    <td> </td>
    <td>Element which has attributes (see above).
Specifies a chart item for a chart component.</td>
  </tr>
</table>


#### 6.34.3. LineChart

The LineChart component represents data items as points connected by a continuous line.

 

Tagname: **_linechart_**

 

Example:

<table>
  <tr>
    <td>month</td>
    <td>profit</td>
    <td>expenses</td>
  </tr>
  <tr>
    <td>Jan</td>
    <td>2000</td>
    <td>1500</td>
  </tr>
  <tr>
    <td>Feb</td>
    <td>1000</td>
    <td>200</td>
  </tr>
  <tr>
    <td>Mar</td>
    <td>1500</td>
    <td>500</td>
  </tr>
  <tr>
    <td>Apr</td>
    <td>1800</td>
    <td>1200</td>
  </tr>
  <tr>
    <td>May</td>
    <td>2400</td>
    <td>575</td>
  </tr>
</table>


![image alt text](assets/images/image_6_32.png?raw=true)

                           

qaml code:

`<linechart legend="right">`

      `<category-axis displayname="Monthly" name="month" />`

      `<linear-axis min-value="200" max-value="3000" ticksize="200" />`

      `<chart-item displayname="Profit" name="profit" />`

      `<chart-item displayname="Expenses" name="expenses" />`

`</linechart>`

 

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
    <td>Text to appear as title.
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
    <td>legend</td>
    <td> </td>
    <td>right</td>
    <td>Specifies the position of the legend with respect to the chart component.
The possible values are:
-         top: place above the chart component, lays out horizontally
-         left: place on the left side of the chart component, lays out vertically
-         bottom: place below chart component, lays out horizontally
-         right: place on the right side of the chart component, lays out vertically
-         none: no legend
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
  <tr>
    <td> </td>
    <td> </td>
    <td> </td>
    <td> </td>
  </tr>
  <tr>
    <td>category-axis</td>
    <td>1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Lets a chart represent data grouped by a set of values along an axis. It represents a horizontal axis of the LineChart component.</td>
  </tr>
  <tr>
    <td>linear-axis</td>
    <td>0..1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Maps numeric values evenly between a minimum and maximum value along an axis. It represents a vertical axis of the LineChart component.</td>
  </tr>
  <tr>
    <td>chart-item</td>
    <td>1..N</td>
    <td> </td>
    <td>Element which has attributes (see above).
Specifies a chart item for a chart component.</td>
  </tr>
</table>


 

           	          	          	          	          	          	          	          	          	          	          	          	            

 

           	          	          	          	          	            

#### 6.34.4. PieChart

The PieChart component represents data items as a standard pie chart. 

 

Tagname: **_piechart_**

 

Example:

<table>
  <tr>
    <td>month</td>
    <td>profit</td>
    <td>expenses</td>
  </tr>
  <tr>
    <td>Jan</td>
    <td>2000</td>
    <td>1500</td>
  </tr>
  <tr>
    <td>Feb</td>
    <td>1000</td>
    <td>200</td>
  </tr>
  <tr>
    <td>Mar</td>
    <td>1500</td>
    <td>500</td>
  </tr>
  <tr>
    <td>Apr</td>
    <td>1800</td>
    <td>1200</td>
  </tr>
  <tr>
    <td>May</td>
    <td>2400</td>
    <td>575</td>
  </tr>
</table>


![image alt text](assets/images/image_6_33.png?raw=true)

                           

qaml code:

`<piechart legend="none">`

      `<category-axis name="month" />`

      `<chart-item displayname="Profit" name="profit" />`

`</piechart>`

 

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
    <td>Text to appear as title.
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
    <td>legend</td>
    <td> </td>
    <td>right</td>
    <td>Specifies the position of the legend with respect to the chart component.
The possible values are:
-         top: place above the chart component, lays out horizontally
-         left: place on the left side of the chart component, lays out vertically
-         bottom: place below chart component, lays out horizontally
-         right: place on the right side of the chart component, lays out vertically
-         none: no legend
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
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camel-case).
 
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
    <td>category-axis</td>
    <td>1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Lets a chart represent data grouped by a set of values along an axis.</td>
  </tr>
  <tr>
    <td>chart-item</td>
    <td>1..N</td>
    <td> </td>
    <td>Element which has attributes (see above).
Specifies a chart item for a chart component.</td>
  </tr>
</table>


 

#### 6.34.5. PlotChart

The PlotChart component represents data items as points.

 

Tagname: **_plotchart_**

 

Example:

<table>
  <tr>
    <td>month</td>
    <td>profit</td>
    <td>expenses</td>
  </tr>
  <tr>
    <td>Jan</td>
    <td>2000</td>
    <td>1500</td>
  </tr>
  <tr>
    <td>Feb</td>
    <td>1000</td>
    <td>200</td>
  </tr>
  <tr>
    <td>Mar</td>
    <td>1500</td>
    <td>500</td>
  </tr>
  <tr>
    <td>Apr</td>
    <td>1800</td>
    <td>1200</td>
  </tr>
  <tr>
    <td>May</td>
    <td>2400</td>
    <td>575</td>
  </tr>
</table>


![image alt text](assets/images/image_6_34.png?raw=true)

                           

qaml code:

`<plotchart legend="none">`

      `<category-axis name="month" />`

      `<chart-item displayname="Profit" name="profit" />`

      `<chart-item displayname="Expenses" name="expenses" />`

`</plotchart>`

 

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
If true, it can not accept user interactions and the component will be greyed out.
 </td>
  </tr>
  <tr>
    <td>displayname</td>
    <td> </td>
    <td> </td>
    <td>Text to appear as title.
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
    <td>legend</td>
    <td> </td>
    <td>right</td>
    <td>Specifies the position of the legend with respect to the chart component.
The possible values are:
-         top: place above the chart component, lays out horizontally
-         left: place on the left side of the chart component, lays out vertically
-         bottom: place below chart component, lays out horizontally
-         right: place on the right side of the chart component, lays out vertically
-         none: no legend
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
           	          	          	          	            
The value of the style needs to follow the css standards (lowercase, '-' divider, no camel-case).
 
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
    <td>category-axis</td>
    <td>1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Lets a chart represent data grouped by a set of values along an axis. It represents a horizontal axis of the PlotChart component.</td>
  </tr>
  <tr>
    <td>linear-axis</td>
    <td>0..1</td>
    <td> </td>
    <td>Element which has attributes (see above).
Maps numeric values evenly between a minimum and maximum value along an axis. It represents a vertical axis of the PlotChart component.</td>
  </tr>
  <tr>
    <td>chart-item</td>
    <td>1..N</td>
    <td> </td>
    <td>Element which has attributes (see above).
Specifies a chart item for a chart component.</td>
  </tr>
</table>


 

