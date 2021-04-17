---
title: Group-Element
description: Stellt ein Gruppen Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Windows-Menüband für Gruppenelement
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390642"
---
# <a name="group-element"></a>Group-Element

Stellt ein [Gruppen](windowsribbon-controls-group.md) Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.

## <a name="usage"></a>Verbrauch

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
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Applicationmodes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Sizedefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wenn angegeben, wird der Wert von <em>sizedefinition</em> auf eine der <a href="windowsribbon-templates.md">Layoutvorlagen</a> beschränkt, die im Menüband-Framework definiert sind. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine beliebige Sequenz von NULL oder mehr Zeichen.<br/> Die maximale Länge ist unbegrenzt.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**Inribbongallery**](windowsribbon-element-inribbongallery.md)<br/>         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Sizedefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                             |
|-----------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**Register**](windowsribbon-element-tab.md) Kartenelement einmal oder mehrmals vorkommen.

[**Registerkarte**](windowsribbon-element-tab.md) unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).

Das Menü Band Markup ist nur gültig, wenn die untergeordneten Elemente der **Gruppe** der für *sizedefinition* angegebenen Vorlage entsprechen.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel veranschaulicht die Verwendung einer benutzerdefinierten Vorlage in einer **Gruppe**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
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
</dt> <dt>

[Gruppen Steuerelement](windowsribbon-controls-group.md)
</dt> <dt>

[**Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

