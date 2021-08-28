---
title: MenuGroup-Element
description: Stellt einen Container von Steuerelementen dar, die in einem Katalog, Menü oder einer Symbolleiste angezeigt werden.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup-Element Windows Menüband
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dad52aebe4a90d132827f01400fc7a1f2bbf1fde
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624716"
---
# <a name="menugroup-element"></a>MenuGroup-Element

Stellt einen Container von Steuerelementen dar, die in einem Katalog, Menü oder einer Symbolleiste angezeigt werden.

## <a name="usage"></a>Verwendung

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>Klasse</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Gibt die Größe und den Layoutstil für Elemente in der Menübenutzeroberfläche an.<br/> Eine Bildressource kann in zwei Größen (groß und klein) bereitgestellt und dem Element im Markup mithilfe der <a href="windowsribbon-element-command-largeimages.md"><strong>Eigenschaftenelemente Command.LargeImages</strong></a> und <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> zugeordnet werden. Wenn nur ein Image bereitgestellt wird, wird die Größe des Frameworks nach Bedarf geändert.<br/> Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems)<br/> </dt> <dd> Standard. <br/> Stil: kleines Bild und hervorgehobener Text.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems)<br/> </dt> <dd> Stil: großes Bild und fett formatierten Text.<br/>
<blockquote>
[!Note]<br />
Wenn <strong>MenuGroup</strong> ein untergeordnetes <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu-Attribut</strong></a>ist, wird das <em>Class-Attribut</em> ignoriert, und ein Stil von <code>MajorItems</code> wird vom Framework erzwungen.
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
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



| Element                                                                             | Beschreibung                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Kombinationsfeld**](windowsribbon-element-combobox.md)<br/>                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Kann nur einmal auftreten.<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss mindestens einmal für jedes [**ApplicationMenu-,**](windowsribbon-element-applicationmenu.md) [**ContextMenu-,**](windowsribbon-element-contextmenu.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery.MenuGroups-,**](windowsribbon-element-dropdowngallery-menugroups.md) [**InRibbonGallery.MenuGroups-,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups-,**](windowsribbon-element-splitbutton-menugroups.md) [**MiniToolbar-**](windowsribbon-element-minitoolbar.md)oder [**SplitButtonGallery.MenuGroups-Element**](windowsribbon-element-splitbuttongallery-menugroups.md) auftreten.

Wenn [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist, **ist MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).

Wenn [**ContextMenu,**](windowsribbon-element-contextmenu.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery.MenuGroups,**](windowsribbon-element-dropdowngallery-menugroups.md) [**InRibbonGallery.MenuGroups,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)oder [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) das übergeordnete Element ist, ist **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button,**](windowsribbon-element-button.md) [**CheckBox,**](windowsribbon-element-checkbox.md) **DropDownButton,** [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md).

Wenn [**MiniToolbar**](windowsribbon-element-minitoolbar.md) das übergeordnete Element ist, **ist MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md).

Das Class-Attribut ist nicht erforderlich, [**wenn ApplicationMenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist. Das Framework erzwingt den Wert MajorItems für das Class-Attribut.

Wenn [**ApplicationMenu das**](windowsribbon-element-applicationmenu.md) übergeordnete Element ist, ist das Class-Attribut nicht erforderlich.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**splitButton mit**](windowsribbon-element-splitbutton.md) einem **MenuGroup-Element** veranschaulicht.

Dieser Codeabschnitt zeigt die [**Befehlsdeklarationen SplitButton**](windowsribbon-element-splitbutton.md) und **MenuGroup** mit einer großen und einer kleinen Bildressource. Eine [**zugeordnete Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButton-Element** fungiert, wird ebenfalls deklariert.


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



Dieser Codeabschnitt zeigt die [**SplitButton-**](windowsribbon-element-splitbutton.md) und **MenuGroup-Steuerelementdeklarationen** mit und `StandardItems` `MajorItems` .


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

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)
</dt> <dt>

[Menügruppe](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





