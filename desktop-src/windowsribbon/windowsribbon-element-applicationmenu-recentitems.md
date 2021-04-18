---
title: Applicationmenu. recentitems (Eigenschaft)
description: Stellt einen Container für das Steuerelement "zuletzt verwendete Elemente" im Anwendungsmenü dar.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Applicationmenu. recentitems-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391947"
---
# <a name="applicationmenurecentitems-property"></a>Applicationmenu. recentitems (Eigenschaft)

Stellt einen Container für das Steuerelement " [zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) " im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
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
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | BESCHREIBUNG                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**"Recentitems"**](windowsribbon-element-recentitems.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                     |
|-----------------------------------------------------------------------------|
| [**Applicationmenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**applicationmenu**](windowsribbon-element-applicationmenu.md) -Element auftreten.

Das Steuerelement zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menüband-Anwendung an.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das Steuerelement " [zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) " veranschaulicht.

Das folgende Beispiel zeigt eine Deklaration eines [**recentitems**](windowsribbon-element-recentitems.md) -Befehls.


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



Das folgende Beispiel zeigt die zugehörige **applicationmenu. recentitems** -und die [**recentitems**](windowsribbon-element-recentitems.md) -Steuerelement Deklaration.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungsmenü-Steuerelement](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Steuerelement für letzte Elemente](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





