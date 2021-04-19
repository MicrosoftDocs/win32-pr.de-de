---
title: Groupsizedefinition-Element
description: Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Groupsizedefinition-Element Windows-Menüband
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339461"
---
# <a name="groupsizedefinition-element"></a>Groupsizedefinition-Element

Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.

## <a name="usage"></a>Verbrauch

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
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
<td><strong>Größe</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Viele<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Mittelalter<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Zuletzt<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                 | BESCHREIBUNG                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Columnbreak**](windowsribbon-element-columnbreak.md)<br/>                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>                   | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Controlsizedefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Zeile**](windowsribbon-element-row.md)<br/>                                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                   |
|---------------------------------------------------------------------------|
| [**Sizedefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Element (einmal pro *Größe*) bis zu drei mal vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird eine grundlegende benutzerdefinierte Vorlage veranschaulicht, die die drei Gruppen layoutgrößen enthält, die beim Erstellen einer benutzerdefinierten Vorlage mit dem **groupsizedefinition** -Element definiert werden müssen.


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

 

 





