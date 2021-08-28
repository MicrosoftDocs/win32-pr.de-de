---
title: Group-Element
description: Stellt ein Gruppensteuerelement dar, das als Container für eine Gruppe von Elementen fungiert.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Group-Element Windows Menüband
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86d12ddb781ecf7e1effba1cade8eb00e92fe20b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631368"
---
# <a name="group-element"></a>Group-Element

Stellt ein [Gruppensteuerelement](windowsribbon-controls-group.md) dar, das als Container für eine Gruppe von Elementen fungiert.

## <a name="usage"></a>Verwendung

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wenn angegeben, wird der Wert von <em>SizeDefinition</em> auf eine der <a href="windowsribbon-templates.md">Layoutvorlagen</a> beschränkt, die vom Menübandframework definiert werden. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Jede Sequenz von 0 (null) oder mehr Zeichen.<br/> Die maximale Länge ist nicht gebunden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | Beschreibung                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Kombinationsfeld**](windowsribbon-element-combobox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Kann höchstens einmal auftreten.<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Kann höchstens einmal auftreten.<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                             |
|-----------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**Tab-Element**](windowsribbon-element-tab.md) auftreten.

[**Registerkarte**](windowsribbon-element-tab.md) unterstützt [Anwendungsmodi.](ribbon-applicationmodes.md)

Das Menübandmarkup ist nur gültig, wenn die untergeordneten Elemente von **Group** der für *SizeDefinition* angegebenen Vorlage entsprechen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Verwendung einer benutzerdefinierten Vorlage in einer **Gruppe** veranschaulicht.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> <dt>

[Gruppensteuerelement](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

