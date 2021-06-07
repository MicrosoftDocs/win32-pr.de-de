---
title: InRibbonGallery-Element
description: Stellt den In-Ribbon Katalog dar, ein katalogbasiertes Steuerelement, das eine Standardteilmenge von Elementen direkt im Menüband verfügbar macht. Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdownmenüschaltfläche geklickt wird.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443371"
---
# <a name="inribbongallery-element"></a>InRibbonGallery-Element

Stellt den [Katalog im Menüband dar,](windowsribbon-controls-inribbongallery.md)ein katalogbasiertes Steuerelement, das eine Standardteilmenge von Elementen direkt im Menüband verfügbar macht. Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdownmenüschaltfläche geklickt wird.

## <a name="usage"></a>Verwendung

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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.
</blockquote>
<br/> Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Itemheight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Bestimmt zusammen <em>mit ItemWidth</em>die Größe des Elementbilds, das im Katalogsteuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich ist. <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Bestimmt zusammen <em>mit ItemHeight</em>die Größe des Elementbilds, das im Katalogsteuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich ist. <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl von Spalten an, die <strong>in InRibbonGallery</strong> angezeigt werden, z. B. in der Dropdownliste Großes Gruppenlayout. <em></em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl von Spalten an, die <strong>die InRibbonGallery</strong> im <em>Gruppenlayout</em> Mittel anzeigt, bevor sie zu <em>Großes Layout</em> wechselt. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die maximale Anzahl von Zeilen für das Layout von <strong>InRibbonGallery-Elementen</strong> an. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standardwert ist 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Mindestanzahl von Spalten an, die die <em></em> <strong>InRibbonGallery</strong> im Layout der großen Gruppe anzeigt, bevor sie zu <em>Medium wechselt.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Mindestanzahl von Spalten an, die <strong>in DerRibbonGallery</strong> im <em>Gruppenlayout</em> Mittel angezeigt wird, bevor zu <em>Small</em>wechselt.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Nein<br/></td>
<td>Gibt an, wo die Elementbezeichnung relativ zum Bild angezeigt wird. <br/> Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Unten)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Ausblenden)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Links)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Überlappung)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Rechts)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Oben)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Typ</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Elemente)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Befehle)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                           | BESCHREIBUNG                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Muss genau einmal auftreten<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Kann nur einmal auftreten.<br/> <br/>      |
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                       | Kann ein oder mehrere Male auftreten.<br/> <br/> |
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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und neuer.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Dies ist optional.

Kann höchstens einmal für jedes [**ControlGroup-**](windowsribbon-element-controlgroup.md) oder [**Group-Element**](windowsribbon-element-group.md) auftreten.

Der folgende Screenshot veranschaulicht das [Menüband-In-Ribbon Gallery-Steuerelement](windowsribbon-controls-inribbongallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Katalog-Steuerelements im Menüband im Microsoft-Farbband.](images/controls/inribbongallery.png)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für einen [Katalog im Menüband](windowsribbon-controls-inribbongallery.md)veranschaulicht.

Dieser Codeabschnitt zeigt die **InRibbonGallery-Befehlsdeklarationen** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **InRibbonGallery-Element** fungiert.


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



Dieser Codeabschnitt zeigt die **InRibbonGallery-Steuerelementdeklarationen.**


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


* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Katalogsteuerelement im Menüband](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> <dt>

[Katalogbeispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





