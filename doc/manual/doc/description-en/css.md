title: CSS
---

Using CSS with the speedata Publisher
=====================================

_Remark: The support of CSS was introduced in version 2.2. At that time, it is more a proof-of-concept than a full implementation. The interface might change in the future. When in doubt, just ask._

Loading a stylesheet and declaring CSS rules
--------------------------------------------

CSS Stylesheets are defined with the command `Stylesheet`:



    <Stylesheet filename="rules.css"/>


or

    <Stylesheet>
      td {
        vertical-align: top ;
      }
    </Stylesheet>

With these rules, some of the XML elements in the layout stylesheet (currently `Box`, `Frame`, `Paragraph`, `Tablerule`, `Td`) can be styled. As it is common with CSS, you can set the properties with the class name, the id and the command name.

For this table

    <ObjektAusgeben>
      <Tabelle>
        <Tr minhöhe="4">
          <Td class="myclass" id="myid"><Absatz><Wert>Hallo Welt</Wert></Absatz></Td>
        </Tr>
      </Tabelle>
    </ObjektAusgeben>

each of the following CSS declarations have the same effect:

````
#myid {
  vertical-align: top ;
}
````

````
.myclass {
  vertical-align: top ;
}
````

und

    td {
      vertical-align: top ;
    }

The mapping of the command names for the CSS rules and the layout rules are documented in the reference manual.
