---
title: FlowMenuLayout-Element
description: Stellt ein horizontales Layout mit Zeilenumbrüchen für Elemente in einem Katalog dar.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- FlowMenuLayout-Element Windows Menüband
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03497e7249937be48b2156d674ac42b88eae68e64982b84344cfe9a935a92e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329080"
---
# <a name="flowmenulayout-element"></a>FlowMenuLayout-Element

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
<th>attribute</th>
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
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Eine beliebige positive oder negative ganze Zahl. <br/> Der Standardwert ist <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Greifer</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Ein Anfügehandle für die Größenänderung, das an die Dropdown-Dropdown-Datei des Katalogs angefügt ist. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Keine)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Vertikal)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Ecke)<br/> </dt> <dd> Standard. <br/> </dd> </dl></td>
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

Das [**VerticalMenuLayout-Element**](windowsribbon-element-verticalmenulayout.md) oder das **FlowMenuLayout-Element** muss einmal für jedes [**DropDownGallery.MenuLayout-,**](windowsribbon-element-dropdowngallery-menulayout.md) [**InRibbonGallery.MenuLayout-**](windowsribbon-element-inribbongallery-menulayout.md)oder [**SplitButtonGallery.MenuLayout-Element**](windowsribbon-element-splitbuttongallery-menulayout.md) auftreten.

Elemente werden entsprechend den Zeilenumbrucheigenschaften angeordnet, die den *Zeilen-* und *Spaltenattributen* inhärent sind. Wenn der Inhalt die Länge einer einzelnen Zeile überschreitet, unterbricht das Menü Zeilen, umschließt Zeilen und richtet den Inhalt entsprechend aus.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**dropDownGallery**](windowsribbon-element-dropdowngallery.md)veranschaulicht.

Dieser Codeabschnitt zeigt die [**DropDownGallery.MenuLayout-Steuerelementdeklaration**](windowsribbon-element-dropdowngallery-menulayout.md) mit einer **FlowMenuLayout-Spezifikation.**


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
* **Kann leer sein:** Ja


 

 





