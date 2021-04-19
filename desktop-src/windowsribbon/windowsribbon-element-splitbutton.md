---
title: SplitButton-Element
description: Stellt ein Standard Steuerelement für unterteilte Schaltflächen dar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Fensterleiste des SplitButton-Elements
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337237"
---
# <a name="splitbutton-element"></a>SplitButton-Element

Stellt ein Standard Steuerelement für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen dar.

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



| Element                                                                                   | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                 | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                             | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| **SplitButton**<br/>                                                                | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**SplitButton. buttonitem**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, **SplitButton**-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.

**SplitButton** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md) , wenn es in der linken Spalte des Anwendungs Menüs gehostet wird.

[**Dropdowngallery**](windowsribbon-element-dropdowngallery.md) und [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von [**DropDownButton**](windowsribbon-element-dropdownbutton.md) , wenn **DropDownButton** ein Nachfolger von [**applicationmenu**](windowsribbon-element-applicationmenu.md)ist.

[**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md) muss einmal auftreten, wenn Folgendes nicht als untergeordnete Elemente von **SplitButton** vorhanden ist:

-   [**Gedrückt**](windowsribbon-element-button.md)
-   [**CheckBox**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)
-   [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Diese Steuerelemente werden als untergeordnete Elemente eines einzelnen standardmäßigen [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md) -Elements behandelt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.

Dieser Code Abschnitt zeigt die **SplitButton** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert.


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



In diesem Code Abschnitt werden die Deklarationen des **SplitButton** -Steuer Elements angezeigt.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerelement "Split Button](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

