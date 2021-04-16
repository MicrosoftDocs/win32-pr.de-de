---
title: Dropdowngallery-Element
description: Stellt ein Drop-Down Katalog-Steuerelement mit einem Galerie basierten Menü dar.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Dropdowngallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516841"
---
# <a name="dropdowngallery-element"></a>Dropdowngallery-Element

Stellt ein [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement mit einem Galerie basierten Menü dar.

## <a name="usage"></a>Verbrauch

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
<tr class="odd">
<td><strong>Haslargeitems</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Galerien, bei denen der Wert des <em>Type</em> -Attributs gleich ist <code>Command</code> .
</blockquote>
<br/> Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Textposition</strong><br/></td>
<td>Textpositiontype<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Unten<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Barg<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Linken<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Überlappen<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Rechten<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Oben<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Type</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Punkte<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Respekt<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                           | BESCHREIBUNG                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Dropdowngallery. menugroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | Muss genau einmal auftreten<br/> <br/>     |
| [**Dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Kann ein-oder mehrmals vorkommen<br/> <br/> |



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
<td><a href="windowsribbon-element-controlgroup.md"><strong>Controlgroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>
<td>, Wenn Sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>applicationmenu</strong></a>enthalten sind. Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente aufweisen.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-oder [**SplitButton**](windowsribbon-element-splitbutton.md) -Element einmal oder mehrmals vorkommen.

**Dropdowngallery** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).

Der folgende Screenshot veranschaulicht das Menüband [-Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.

![Screenshot eines Dropdown Galerie-Steuer Elements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für **dropdowngallery** veranschaulicht.

Dieser Code Abschnitt zeigt die **dropdowngallery** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **dropdowngallery** -Element fungiert.


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



In diesem Code Abschnitt werden die Deklarationen des **dropdowngallery** -Steuer Elements veranschaulicht.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Dropdown-Katalog-Steuerelement**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Arbeiten mit Galerien](ribbon-controls-galleries.md)
</dt> <dt>

[**Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Galerie Beispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

