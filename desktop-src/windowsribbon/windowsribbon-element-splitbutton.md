---
title: SplitButton-Element
description: Stellt ein Standardmäßiges Split Button-Steuerelement dar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- SplitButton-Element Windows Menüband
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53445bc3f57f8a861800f9edcd95d8af2ecfbd54f4055cf8787695dab1f25cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850772"
---
# <a name="splitbutton-element"></a>SplitButton-Element

Stellt ein Standardmäßiges [Split Button-Steuerelement](windowsribbon-controls-splitbutton.md) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
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
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Nur gültig, <a href="windowsribbon-element-menugroup.md"><strong>wenn MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerzeichen sind gültig und werden ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                 | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                             | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| **SplitButton**<br/>                                                                | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Kann nur einmal auftreten.<br/> <br/>      |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Kann nur einmal auftreten.<br/> <br/>      |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) **SplitButton-** oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.

**SplitButton unterstützt** [Anwendungsmodi,](ribbon-applicationmodes.md) wenn es in der linken Spalte des Anwendungsmenüs gehostet wird.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) und [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) wenn **DropDownButton** ein Nachfolger von [**ApplicationMenu ist.**](windowsribbon-element-applicationmenu.md)

[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) muss einmal auftreten, wenn folgende Elemente nicht als untergeordnete Elemente von **SplitButton vorhanden sind:**

-   [**Schaltfläche**](windowsribbon-element-button.md)
-   [**Checkbox**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
-   [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Diese Steuerelemente werden als untergeordnete Elemente eines einzelnen [**SplitButton.MenuGroups-Standardelements**](windowsribbon-element-splitbutton-menugroups.md) behandelt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die [Split-Schaltfläche veranschaulicht.](windowsribbon-controls-splitbutton.md)

In diesem Codeabschnitt werden die **Deklarationen des SplitButton-Befehls** mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) gezeigt, die als übergeordneter Container für das **SplitButton-Element** fungiert.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



In diesem Codeabschnitt werden die **SplitButton-Steuerelementdeklarationen** gezeigt.


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>Elementinformationen

- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerelement "Schaltfläche teilen"](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

