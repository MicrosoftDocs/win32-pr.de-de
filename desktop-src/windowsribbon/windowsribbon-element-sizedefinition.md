---
title: Sizedefinition-Element
description: Stellt eine benutzerdefinierte Layoutvorlage von Menü Band Steuerelementen dar.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Fenster "sizedefinition-Element Windows"
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340883"
---
# <a name="sizedefinition-element"></a>Sizedefinition-Element

Stellt eine benutzerdefinierte Layoutvorlage von Menü Band Steuerelementen dar.

## <a name="usage"></a>Verbrauch

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Name</strong><br/></td>
<td>xs: positiveInteger oder xs: String oder xs: Token<br/></td>
<td>Ja<br/></td>
<td>, Wenn <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Menüband. sizedefinitions</strong></a> das übergeordnete Element ist, andernfalls optional.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger oder xs: String oder xs: Token)<br/> </dt> <dd> Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | BESCHREIBUNG                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**Controlnamemap**](windowsribbon-element-controlnamemap.md)<br/>           | Kann höchstens einmal vorkommen<br/> <br/>   |
| [**Groupsizedefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Muss mindestens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Gruppe**](windowsribbon-element-group.md)<br/>                                   |
| [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Group**](windowsribbon-element-group.md) -Element auftreten.

Kann für jedes [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element einmal oder mehrmals vorkommen.

Vordefinierte [Layoutvorlagen](windowsribbon-templates.md) für das Menüband-Framework werden mit dem *sizedefinition* -Attribut des [**Group**](windowsribbon-element-group.md) -Elements angegeben.

Wenn ein entsprechendes [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -Element nicht für jedes [**Group**](windowsribbon-element-group.md) -Element in einem [**Register**](windowsribbon-element-tab.md) Kartenelement deklariert wird, tritt ein Validierungs Fehler auf.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird eine grundlegende benutzerdefinierte Vorlage veranschaulicht.


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





