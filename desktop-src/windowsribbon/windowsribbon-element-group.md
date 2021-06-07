---
title: Group-Element
description: Stellt ein Group-Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Gruppenelement Windows-Menüband
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442871"
---
# <a name="group-element"></a>Group-Element

Stellt ein [Group-Steuerelement](windowsribbon-controls-group.md) dar, das als Container für eine Gruppe von Elementen fungiert.

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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerzeichen sind gültig und werden ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wenn angegeben, ist der Wert von <em>SizeDefinition</em> auf eine der Layoutvorlagen beschränkt, <a href="windowsribbon-templates.md">die</a> vom Menübandframework definiert werden. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine beliebige Sequenz von null oder mehr Zeichen.<br/> Die maximale Länge ist ungebunden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Kann nur einmal auftreten.<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Kann nur einmal auftreten.<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                             |
|-----------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann ein oder mehrere Male für jedes [**Tab-Element**](windowsribbon-element-tab.md) auftreten.

[**Die Registerkarte**](windowsribbon-element-tab.md) unterstützt [die Anwendungsmodi](ribbon-applicationmodes.md).

Das Menübandmarkup ist nur gültig, wenn die untergeordneten Elemente von **Group** der für *SizeDefinition angegebenen Vorlage entsprechen.*

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Verwendung einer benutzerdefinierten Vorlage in einer **Gruppe veranschaulicht.**


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> <dt>

[Gruppensteuerung](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

