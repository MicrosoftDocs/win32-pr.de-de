---
title: GroupSizeDefinition-Element
description: Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition-Element Windows Menüband
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc3184f18bf692c333d7088ade79ff4ac5360f1a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631358"
---
# <a name="groupsizedefinition-element"></a>GroupSizeDefinition-Element

Stellt eine Layoutgröße für eine Gruppe von Steuerelementen in einer benutzerdefinierten Vorlage dar.

## <a name="usage"></a>Verwendung

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Größe</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Groß)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (Mittel)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Klein)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                 | Beschreibung                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ColumnBreak**](windowsribbon-element-columnbreak.md)<br/>                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                   | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Zeile**](windowsribbon-element-row.md)<br/>                                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                   |
|---------------------------------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann bis zu dreimal für jedes [**SizeDefinition-Element**](windowsribbon-element-sizedefinition.md) auftreten (einmal für jede *Größe*).

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel veranschaulicht eine einfache benutzerdefinierte Vorlage, die die drei Gruppenlayoutgrößen enthält, die beim Erstellen einer benutzerdefinierten Vorlage mit dem **GroupSizeDefinition-Element** definiert werden müssen.


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

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





