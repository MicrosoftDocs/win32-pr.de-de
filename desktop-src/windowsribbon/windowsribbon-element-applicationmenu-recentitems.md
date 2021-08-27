---
title: ApplicationMenu.RecentItems-Eigenschaft
description: Stellt einen Container für das Steuerelement Zuletzt verwendete Elemente im Anwendungsmenü dar.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- ApplicationMenu.RecentItems-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630375"
---
# <a name="applicationmenurecentitems-property"></a>ApplicationMenu.RecentItems-Eigenschaft

Stellt einen Container für das Steuerelement [Zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md) im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.

## <a name="usage"></a>Verwendung

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
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
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
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | Beschreibung                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**RecentItems**](windowsribbon-element-recentitems.md)<br/> | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**ApplicationMenu-Element**](windowsribbon-element-applicationmenu.md) auftreten.

Das Steuerelement Zuletzt verwendete [Elemente](windowsribbon-controls-recentitems.md) zeigt die Liste der zuletzt verwendeten Elemente (MRU) der Menübandanwendung an.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das [Steuerelement Recent Items](windowsribbon-controls-recentitems.md) veranschaulicht.

Das folgende Beispiel zeigt eine [**RecentItems**](windowsribbon-element-recentitems.md) Command-Deklaration.


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



Das folgende Beispiel zeigt die zugeordnete Deklaration der **Steuerelemente ApplicationMenu.RecentItems** und [**RecentItems.**](windowsribbon-element-recentitems.md)


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anwendungsmenü-Steuerelement](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Steuerelement "Zuletzt durchgeführte Elemente"](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





