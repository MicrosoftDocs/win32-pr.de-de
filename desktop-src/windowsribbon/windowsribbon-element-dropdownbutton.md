---
title: DropDownButton-Element
description: Stellt ein standardmäßiges Drop-Down Button-Steuerelement dar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- DropDownButton-Element Windows Menüband
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08353f4d6c743d92eff08f83e90babb9cc9d075f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623926"
---
# <a name="dropdownbutton-element"></a>DropDownButton-Element

Stellt ein standardmäßiges [Dropdown-Schaltflächen-Steuerelement](windowsribbon-controls-dropdownbutton.md) dar.

## <a name="usage"></a>Verwendung

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
<td>Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                             | Beschreibung                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**Kombinationsfeld**](windowsribbon-element-combobox.md)<br/>                       | Kann ein oder mehrere Male auftreten<br/> <br/> |
| **DropDownButton**<br/>                                                       | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                     | Muss mindestens einmal auftreten.<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein oder mehrere Male auftreten<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein oder mehrere Male auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional oder erforderlich, je nach übergeordnetem Element.

Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) **DropDownButton-,** [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-, MenuGroup-,**](windowsribbon-element-menugroup.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten. [](windowsribbon-element-group.md)

**DropDownButton** unterstützt [Anwendungsmodi,](ribbon-applicationmodes.md) wenn es in der linken Spalte des Anwendungsmenüs gehostet wird.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) und [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von **DropDownButton,** wenn **DropDownButton** ein Nachfolger von [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für **dropDownButton** veranschaulicht.

Dieser Codeabschnitt zeigt die **DropDownButton-Befehlsdeklarationen** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **DropDownButton-Element** fungiert.


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



Dieser Codeabschnitt zeigt die **DropDownButton-Steuerelementdeklarationen.**


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

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Dropdown-Schaltflächen-Steuerelement](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

