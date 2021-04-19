---
title: Flowmenulayout-Element
description: Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Flowmenulayout-Element Windows-Menüband
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341901"
---
# <a name="flowmenulayout-element"></a>Flowmenulayout-Element

Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.

## <a name="usage"></a>Verbrauch

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
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
<td><strong>Spalten</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Anzahl der Elemente an, die in einer einzelnen Zeile angezeigt werden sollen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Eine positive oder negative ganze Zahl. <br/> Der Standardwert ist <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Zieh Elements</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Ein an den Katalog-Dropdown angefügtes Handle zur Anpassung der Größe. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Gar<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Rechtes<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Eckpfeiler<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Zeilen</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Anzahl der Element Zeilen an, die ohne Scrollen sichtbar sein sollen. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Eine positive oder negative ganze Zahl. <br/> Der Standardwert ist <strong>-1</strong> . dieser gibt an, dass so viele Element Zeilen wie möglich angezeigt werden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**Dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**Inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**Splitbuttongallery. menulayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Entweder das [**verticalmenulayout**](windowsribbon-element-verticalmenulayout.md) -oder das **flowmenulayout** -Element muss für jedes [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)-, [**inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)-oder [**splitbuttongallery. menulayout**](windowsribbon-element-splitbuttongallery-menulayout.md) -Element einmal vorkommen.

Elemente werden entsprechend den Zeilenumbruch Eigenschaften angeordnet, die *den Zeilen-und* *Spalten* Attributen unterliegen. Wenn Inhalt die Länge einer einzelnen Zeile überschreitet, unterbricht das Menü Zeilen, umschließt Zeilen und richtet Inhalte entsprechend aus.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.

In diesem Code Abschnitt wird die [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md) -Steuerelement Deklaration mit einer **flowmenulayout** -Spezifikation veranschaulicht.


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
| Kann leer bleiben                        | Ja       |



 

 





