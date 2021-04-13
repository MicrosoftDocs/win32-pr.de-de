---
title: Controlgroup-Element
description: Stellt eine Gruppe von Steuerelementen in einer sizedefinition-Layoutvorlage dar.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Windows-Menüband für controlgroup-Element
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389784"
---
# <a name="controlgroup-element"></a>Controlgroup-Element

Stellt eine Gruppe von Steuerelementen in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage dar.

## <a name="usage"></a>Verbrauch

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
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Nur gültig, wenn die <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> das übergeordnete Element ist.<br/> Jede <em>sequencenumkehr</em> muss innerhalb eines <a href="windowsribbon-element-group.md"><strong>Group</strong></a> -Elements eindeutig sein. Die Werte für <em>sequencenenumber</em> sollten für jedes <strong>Group</strong> -Element erhöht werden, müssen jedoch nicht sequenziell sein. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1000 und 59999 (einschließlich).<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                 | BESCHREIBUNG                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                               | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Controlsizedefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**Inribbongallery**](windowsribbon-element-inribbongallery.md)<br/>             | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                             |
|-------------------------------------------------------------------------------------|
| **Controlgroup**<br/>                                                         |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                             |
| [**Groupsizedefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Zeile**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**Group**](windowsribbon-element-group.md) -oder **controlgroup** -Element einmal oder mehrmals vorkommen.

Wenn keine Sequenznummern angegeben werden, werden Elemente in der Reihenfolge gerendert, in der das Menüband-Markup angegeben ist.

Wenn " [**Group**](windowsribbon-element-group.md) " oder " **controlgroup** " das übergeordnete Element ist, wird " **controlgroup** " auf die folgenden möglichen untergeordneten Elemente beschränkt: [**Schaltfläche**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**Dropdown Button**](windowsribbon-element-dropdownbutton.md), [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md), [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)oder UMSCHALT [**Fläche**](windowsribbon-element-togglebutton.md)

Wenn " [**Row**](windowsribbon-element-row.md) " oder " [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) " das übergeordnete Element ist, wird die [**Gruppe**](windowsribbon-element-group.md) auf das folgende mögliche untergeordnete Element beschränkt: [**controlsizedefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit verschiedenen [**Gruppen**](windowsribbon-element-group.md) Elementen veranschaulicht.


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

 

 





