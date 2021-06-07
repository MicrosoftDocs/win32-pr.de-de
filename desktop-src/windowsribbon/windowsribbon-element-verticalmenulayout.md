---
title: VerticalMenuLayout-Element
description: Stellt ein vertikales Layout für Elemente in einem Katalog dar.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout-Element Windows-Menüband
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444051"
---
# <a name="verticalmenulayout-element"></a>VerticalMenuLayout-Element

Stellt ein vertikales Layout für Elemente in einem Katalog dar.

## <a name="usage"></a>Verwendung

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Greifer</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Ein Anfügehandle für die Größenänderung, das an die Dropdown-Dropdown-Datei des Katalogs angefügt ist. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Keine)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Vertikal)<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>Nein<br/></td>
<td><strong>Windows 8 und neuer</strong><br/> Hebt alle Elemente in der Liste bis einschließlich des aktuellen Mauszeigerelements hervor (anstatt nur des Mauszeigerelements). Wird in der Regel für mehrere <strong>Rückgängig-</strong> und <strong>Wiederholungsfunktionen</strong> verwendet.<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Zeilen</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td>Gibt die Anzahl der Elementzeilen an, die ohne Bildlauf sichtbar sein sollen. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Eine beliebige positive oder negative ganze Zahl. <br/> Der Standardwert ist <strong>-1,</strong> der angibt, dass so viele Elementzeilen wie möglich angezeigt werden sollen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Das **VerticalMenuLayout-Element** oder das [**FlowMenuLayout-Element**](windowsribbon-element-flowmenulayout.md) muss einmal für jedes [**DropDownGallery.MenuLayout-,**](windowsribbon-element-dropdowngallery-menulayout.md) [**InRibbonGallery.MenuLayout-**](windowsribbon-element-inribbongallery-menulayout.md)oder [**SplitButtonGallery.MenuLayout-Element**](windowsribbon-element-splitbuttongallery-menulayout.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für ein **VerticalMenuLayout-Element** veranschaulicht.

Dieser Codeabschnitt zeigt die [**InRibbonGallery-Steuerelementdeklarationen.**](windowsribbon-element-inribbongallery.md)


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


- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Ja



 

 





