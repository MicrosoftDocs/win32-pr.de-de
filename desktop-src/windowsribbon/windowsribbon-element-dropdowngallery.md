---
title: DropDownGallery-Element
description: Stellt ein Drop-Down Gallery-Steuerelement mit einem katalogbasierten Menü dar.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443421"
---
# <a name="dropdowngallery-element"></a>DropDownGallery-Element

Stellt ein [Dropdownkatalog-Steuerelement](windowsribbon-controls-dropdowngallery.md) mit einem katalogbasierten Menü dar.

## <a name="usage"></a>Verwendung

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
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
<td>Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalogsteuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.
</blockquote>
<br/> Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Itemheight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Unten)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Ausblenden)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Links)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Überlappung)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Rechts)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Oben)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Typ</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Elemente)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Befehle)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                           | BESCHREIBUNG                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                         | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | Muss genau einmal auftreten<br/> <br/>     |
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a><br/></td>
<td>Wenn sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>enthalten ist. Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente enthalten.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und neuer.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**Group-, MenuGroup-**](windowsribbon-element-menugroup.md)oder [**SplitButton-Element**](windowsribbon-element-splitbutton.md) auftreten. [](windowsribbon-element-group.md)

**DropDownGallery** unterstützt [Anwendungsmodi.](ribbon-applicationmodes.md)

Der folgende Screenshot veranschaulicht das [Menüband-Dropdownkatalog-Steuerelement](windowsribbon-controls-dropdowngallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Dropdownkatalog-Steuerelements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für **dropDownGallery** veranschaulicht.

Dieser Codeabschnitt zeigt die **DropDownGallery** Command-Deklarationen mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **DropDownGallery-Element** fungiert.


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



Dieser Codeabschnitt zeigt die **DropDownGallery-Steuerelementdeklarationen.**


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dropdownkatalog-Steuerelement**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Katalogbeispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

