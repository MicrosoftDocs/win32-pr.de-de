---
title: MenuGroup-Element
description: Stellt einen Container von Steuerelementen dar, die in einem Katalog, Menü oder einer Symbolleiste angezeigt werden.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup-Element Windows-Menüband
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103721944"
---
# <a name="menugroup-element"></a>MenuGroup-Element

Stellt einen Container von Steuerelementen dar, die in einem Katalog, Menü oder einer Symbolleiste angezeigt werden.

## <a name="usage"></a>Verbrauch

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
<td><strong>Klasse</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Gibt die Größe und layoutart für Elemente in der Benutzeroberfläche des Menüs an.<br/> Eine Bildressource kann in zwei Größen (groß und klein) bereitgestellt werden und mit dem-Element im Markup verknüpft werden, indem die <a href="windowsribbon-element-command-largeimages.md"><strong>Befehls. largeimages</strong></a> -und <a href="windowsribbon-element-command-smallimages.md"><strong>Command. smallimages</strong></a> -Eigenschaften Elemente verwendet werden. Wenn nur ein Bild bereitgestellt wird, ändert sich das Framework nach Bedarf.<br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Standarditems)<br/> </dt> <dd> Standard. <br/> Stil: kleines Bild und von der hervorgehoben hervorgehobene Text.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (Majoritems)<br/> </dt> <dd> Stil: großes Bild und fett formatierter Text.<br/>
<blockquote>
[!Note]<br />
Wenn <strong>MenuGroup</strong> ein untergeordnetes Element von <a href="windowsribbon-element-applicationmenu.md"><strong>applicationmenu</strong></a>ist, wird das <em>Class</em> -Attribut ignoriert und ein Stil von <code>MajorItems</code> durch das Framework erzwungen.
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
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
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Kann ein-oder mehrmals vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**Applicationmenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**Dropdowngallery. menugroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**Inribbongallery. menugroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**Splitbuttongallery. menugroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss mindestens einmal für jedes [**applicationmenu**](windowsribbon-element-applicationmenu.md)-, [**ContextMenu**](windowsribbon-element-contextmenu.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery. menugroups**](windowsribbon-element-dropdowngallery-menugroups.md)-, [**inribbongallery. menugroups**](windowsribbon-element-inribbongallery-menugroups.md)-, [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md)-, [**MiniToolbar**](windowsribbon-element-minitoolbar.md)-oder [**splitbuttongallery. menugroups**](windowsribbon-element-splitbuttongallery-menugroups.md) -Element erfolgen.

Wenn [**applicationmenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist, wird **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Schaltfläche**](windowsribbon-element-button.md), [**Dropdown Button**](windowsribbon-element-dropdownbutton.md), [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md).

Wenn [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**dropdowngallery. menugroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**inribbongallery. menugroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md)oder [**splitbuttongallery. menugroups**](windowsribbon-element-splitbuttongallery-menugroups.md) ist das übergeordnete Element, dann ist **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Schaltfläche**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **Dropdown Button**, [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md), [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)oder UMSCHALT [**Fläche**](windowsribbon-element-togglebutton.md).

Wenn [**MiniToolbar**](windowsribbon-element-minitoolbar.md) das übergeordnete Element ist, wird **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Schaltfläche**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**Dropdown Button**](windowsribbon-element-dropdownbutton.md), [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md), [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)oder [**degglebutton**](windowsribbon-element-togglebutton.md).

Das Class-Attribut ist nicht erforderlich, wenn [**applicationmenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist. Das Framework erzwingt den Wert von "majoritems" für das Klassen Attribut.

Wenn [**applicationmenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist, ist das Class-Attribut nicht erforderlich.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das [**SplitButton**](windowsribbon-element-splitbutton.md) -Element mit einem **MenuGroup** -Element veranschaulicht.

In diesem Code Abschnitt werden die Befehls Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **MenuGroup** mit einer großen und kleinen Bildressource angezeigt. Eine zugeordnete [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert, wird ebenfalls deklariert.


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



In diesem Code Abschnitt werden die Steuerelement Deklarationen [**SplitButton**](windowsribbon-element-splitbutton.md) und **MenuGroup** mit `StandardItems` und angezeigt `MajorItems` .


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

[Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md)
</dt> <dt>

[Menü Gruppe](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





