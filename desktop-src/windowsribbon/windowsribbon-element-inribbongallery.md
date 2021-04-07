---
title: Inribbongallery-Element
description: Stellt die In-Ribbon-Galerie dar, ein Galerie basiertes Steuerelement, das eine Standard Teilmenge von Elementen direkt im Menüband verfügbar macht. Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdown Menü Schaltfläche geklickt wird.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Inribbongallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "104038717"
---
# <a name="inribbongallery-element"></a>Inribbongallery-Element

Stellt den [in-Ribbon](windowsribbon-controls-inribbongallery.md)-Katalog dar, ein Galerie basiertes Steuerelement, das eine Standard Teilmenge von Elementen direkt im Menüband verfügbar macht. Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdown Menü Schaltfläche geklickt wird.

## <a name="usage"></a>Verbrauch

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
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
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Mit <em>ItemWidth</em>wird die Größe des Element Bilds bestimmt, das im Katalog-Steuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Galerien, bei denen der Wert des <em>Type</em> -Attributs gleich ist. <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>In Verbindung mit <em>ItemHeight</em>wird die Größe des Element Bilds bestimmt, das im Katalog-Steuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Galerien, bei denen der Wert des <em>Type</em> -Attributs gleich ist. <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl der Spalten an, die von <strong>inribbongallery</strong> angezeigt werden, z. b. in der Dropdown-Dropdown-Datei für <em>große</em> Gruppen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Maxcolumnsmedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl der Spalten an, die <strong>inribbongallery</strong> im <em>mittleren</em> Gruppen Layout anzeigt, bevor Sie zu einem <em>großen</em> Layout wechseln. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl von Zeilen für das Layout von <strong>inribbongallery</strong> -Elementen an. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Der Standardwert ist 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Mincolumnslarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Mindestanzahl von Spalten an, die <strong>inribbongallery</strong> im Layout der <em>großen</em> Gruppe anzeigt, bevor Sie zum <em>Mittel</em>Wert wechseln.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Mincolumnsmedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Mindestanzahl von Spalten an, die <strong>inribbongallery</strong> im <em>mittleren</em> Gruppen Layout anzeigt, bevor Sie zu <em>Small</em>wechseln.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Textposition</strong><br/></td>
<td>Textpositiontype<br/></td>
<td>Nein<br/></td>
<td>Gibt an, wo die Element Bezeichnung relativ zum Bild angezeigt wird. <br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
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
| [**Markieren**](windowsribbon-element-checkbox.md)<br/>                                     | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Inribbongallery. menugroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Muss genau einmal auftreten<br/> <br/>     |
| [**Inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |
| [**Gedrückt**](windowsribbon-element-button.md)<br/>                                       | Kann ein-oder mehrmals vorkommen<br/> <br/> |
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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes Element der Gruppe " [**controlgroup**](windowsribbon-element-controlgroup.md) " oder " [**Group**](windowsribbon-element-group.md) " auftreten.

Der folgende Screenshot veranschaulicht das Multifunktionsleisten [-Steuerelement im Menüband-](windowsribbon-controls-inribbongallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.

![Screenshot eines in-Ribbon Gallery-Steuer Elements im Microsoft Paint-Menüband.](images/controls/inribbongallery.png)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für einen [in-Ribbon-](windowsribbon-controls-inribbongallery.md)Katalog veranschaulicht.

Dieser Code Abschnitt zeigt die **inribbongallery** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **inribbongallery** -Element fungiert.


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



In diesem Code Abschnitt werden die Deklarationen des **inribbongallery** -Steuer Elements veranschaulicht.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[In-Ribbon Gallery-Steuerelement](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Arbeiten mit Galerien](ribbon-controls-galleries.md)
</dt> <dt>

[Galerie Beispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





