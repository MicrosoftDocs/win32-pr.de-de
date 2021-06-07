---
title: RecentItems-Element
description: Stellt das Steuerelement Letzte Elemente im Anwendungsmenü dar.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems-Element Windows-Menüband
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444111"
---
# <a name="recentitems-element"></a>RecentItems-Element

Stellt das Steuerelement [Letzte Elemente](windowsribbon-controls-recentitems.md) im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.

## <a name="usage"></a>Verwendung

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
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
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>EnablePinning</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der zuletzt anzuzeigende Elemente.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)<br/> </dt> <dd> Ein ganzzahliger Wert von 0 oder höher.<br/> Der Standardwert ist <strong>10.</strong><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss für jedes [**ApplicationMenu.RecentItems-Element**](windowsribbon-element-applicationmenu-recentitems.md) genau einmal auftreten.

Das Steuerelement Zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menübandanwendung an.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das [Steuerelement Recent Items](windowsribbon-controls-recentitems.md) veranschaulicht.

Das folgende Beispiel zeigt eine **RecentItems** Command-Deklaration.


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



Das folgende Beispiel zeigt die **zugeordnete RecentItems-Steuerelementdeklaration.**


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Ja


## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungsmenü-Steuerelement](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Steuerelement "Zuletzt durchgeführte Elemente"](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





