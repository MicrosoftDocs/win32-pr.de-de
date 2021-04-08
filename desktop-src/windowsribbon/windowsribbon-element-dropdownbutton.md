---
title: DropDownButton-Element
description: Stellt ein Standard-Drop-Down Schaltflächen-Steuerelement dar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Windows-Menüband für DropDownButton-Element
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729224"
---
# <a name="dropdownbutton-element"></a>DropDownButton-Element

Stellt ein Standard [-Dropdown-Schalt](windowsribbon-controls-dropdownbutton.md) Flächen-Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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
<td>Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| **DropDownButton**<br/>                                                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                     | Muss mindestens einmal vorkommen<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Optional oder erforderlich, abhängig vom übergeordneten Element.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, **DropDownButton**-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.

**DropDownButton** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md) , wenn Sie in der linken Spalte des Anwendungs Menüs gehostet werden.

[**Dropdowngallery**](windowsribbon-element-dropdowngallery.md) und [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von **DropDownButton** , wenn **DropDownButton** ein Nachfolger von [**applicationmenu**](windowsribbon-element-applicationmenu.md)ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für **DropDownButton** veranschaulicht.

Dieser Code Abschnitt zeigt die **Dropdown Button** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **Dropdown Button** -Element fungiert.


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



In diesem Code Abschnitt werden die Deklarationen des **Dropdown Button** -Steuer Elements angezeigt.


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Dropdown-Schaltflächen-Steuerelement](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

