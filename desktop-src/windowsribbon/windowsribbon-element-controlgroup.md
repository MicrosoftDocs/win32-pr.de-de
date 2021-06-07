---
title: ControlGroup-Element
description: Stellt eine Gruppe von Steuerelementen in einer SizeDefinition-Layoutvorlage dar.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- ControlGroup-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442941"
---
# <a name="controlgroup-element"></a>ControlGroup-Element

Stellt eine Gruppe von Steuerelementen in einer [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) dar.

## <a name="usage"></a>Verwendung

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
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
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Nur gültig, <a href="windowsribbon-element-group.md"><strong>wenn Group</strong></a> das übergeordnete Element ist.<br/> Jede <em>SequenceNumber</em> muss innerhalb eines Group-Elements <a href="windowsribbon-element-group.md"><strong>eindeutig</strong></a> sein. Die Werte für <em>SequenceNumber</em> sollten für jedes <strong>Group-Element</strong> erhöht werden, müssen jedoch nicht sequenziell sein. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein positiver ganzzahliger Wert zwischen 1000 und 59999 einschließlich .<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                 | BESCHREIBUNG                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Kann nur einmal auftreten.<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>             | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                             |
|-------------------------------------------------------------------------------------|
| **ControlGroup**<br/>                                                         |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                             |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Zeile**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann ein oder mehrere Male für jedes [**Group- oder**](windowsribbon-element-group.md) **ControlGroup-Element** auftreten.

Wenn keine Sequenznummern angegeben werden, werden Elemente in der im Menübandmarkup angegebenen Reihenfolge gerendert.

Wenn [**Group**](windowsribbon-element-group.md) oder **ControlGroup** das übergeordnete Element ist, **ist ControlGroup** auf die folgenden möglichen untergeordneten Elemente beschränkt: [**Button,**](windowsribbon-element-button.md) [**CheckBox,**](windowsribbon-element-checkbox.md) [**ComboBox,**](windowsribbon-element-combobox.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**FontControl,**](windowsribbon-element-fontcontrol.md) [**InRibbonGallery,**](windowsribbon-element-inribbongallery.md) [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md)

Wenn Row [**oder**](windowsribbon-element-row.md) [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) das übergeordnete Element ist, ist [**Group**](windowsribbon-element-group.md) andernfalls auf das folgende mögliche untergeordnete Element [**beschränkt: ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit verschiedenen [**Group-Elementen**](windowsribbon-element-group.md) veranschaulicht.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> </dl>

 

 





