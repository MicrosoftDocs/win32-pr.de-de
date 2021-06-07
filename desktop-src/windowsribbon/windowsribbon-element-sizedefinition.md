---
title: SizeDefinition-Element
description: Stellt eine benutzerdefinierte Layoutvorlage von Menüband-Steuerelementen dar.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- SizeDefinition-Element Windows-Menüband
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444801"
---
# <a name="sizedefinition-element"></a>SizeDefinition-Element

Stellt eine benutzerdefinierte Layoutvorlage von Menüband-Steuerelementen dar.

## <a name="usage"></a>Verwendung

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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Name</strong><br/></td>
<td>xs:positiveInteger oder xs:string oder xs:token<br/></td>
<td>Ja<br/></td>
<td>Wenn <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> das übergeordnete Element ist, andernfalls optional.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string oder xs:token)<br/> </dt> <dd> Eine Zeichenfolge oder ein ganzzahliger Wert zwischen 2 und 59999, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | BESCHREIBUNG                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**ControlNameMap**](windowsribbon-element-controlnamemap.md)<br/>           | Kann höchstens einmal auftreten.<br/> <br/>   |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Muss mindestens einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Gruppe**](windowsribbon-element-group.md)<br/>                                   |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann höchstens einmal für jedes [**Group-Element**](windowsribbon-element-group.md) auftreten.

Kann ein oder mehrere Male für jedes [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) auftreten.

Vordefinierte [Menüband-Frameworklayoutvorlagen](windowsribbon-templates.md) werden mit dem *SizeDefinition-Attribut* des [**Group-Elements**](windowsribbon-element-group.md) angegeben.

Wenn ein [**entsprechendes ScalingPolicy.IdealSizes-Element**](windowsribbon-element-scalingpolicy-idealsizes.md) nicht für jedes [**Group-Element**](windowsribbon-element-group.md) in einem [**Tab-Element**](windowsribbon-element-tab.md) deklariert wird, tritt ein Validierungsfehler auf.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel veranschaulicht eine einfache benutzerdefinierte Vorlage.


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


- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





