---
title: Controlsizedefinition-Element
description: Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Windows-Menüband "controlsizedefinition-Element"
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312660"
---
# <a name="controlsizedefinition-element"></a>Controlsizedefinition-Element

Stellt den Layoutstil einer Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
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
<td><strong>ControlName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ImageSize</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Viele<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Zuletzt<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Isimagevisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Islabelvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Ispopup</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                             |
|-------------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>               |
| [**Groupsizedefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Zeile**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**Row**](windowsribbon-element-row.md)-oder [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Element einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit verschiedenen **controlsizedefinition** -Elementen veranschaulicht.


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
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





