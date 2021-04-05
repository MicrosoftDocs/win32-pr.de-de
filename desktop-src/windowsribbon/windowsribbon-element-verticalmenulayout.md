---
title: Verticalmenulayout-Element
description: Stellt ein vertikales Layout für Elemente in einem Katalog dar.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Windows-Menüband für verticalmenulayout-Element
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724344"
---
# <a name="verticalmenulayout-element"></a>Verticalmenulayout-Element

Stellt ein vertikales Layout für Elemente in einem Katalog dar.

## <a name="usage"></a>Verbrauch

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
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Zieh Elements</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Ein an den Katalog-Dropdown angefügtes Handle zur Anpassung der Größe. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Gar<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Rechtes<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Ismultiplehighlightingenabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>Nein<br/></td>
<td><strong>Windows 8 und höher</strong><br/> Hebt alle Elemente in der Liste bis einschließlich des aktuellen Mouseover-Elements hervor (anstelle des Mouseover-Elements). Wird normalerweise für mehrere Funktionen zum Rückgängigmachen und wieder <strong>holen</strong> <strong></strong><br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
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

Entweder das **verticalmenulayout** -oder das [**flowmenulayout**](windowsribbon-element-flowmenulayout.md) -Element muss für jedes [**dropdowngallery. menulayout**](windowsribbon-element-dropdowngallery-menulayout.md)-, [**inribbongallery. menulayout**](windowsribbon-element-inribbongallery-menulayout.md)-oder [**splitbuttongallery. menulayout**](windowsribbon-element-splitbuttongallery-menulayout.md) -Element einmal vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für ein **verticalmenulayout** -Element veranschaulicht.

In diesem Code Abschnitt werden die Deklarationen des [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuer Elements veranschaulicht.


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
| Kann leer bleiben                        | Ja       |



 

 





