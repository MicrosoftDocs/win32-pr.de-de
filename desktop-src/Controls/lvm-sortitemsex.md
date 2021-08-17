---
title: LVM_SORTITEMSEX (Commctrl.h)
description: Verwendet eine anwendungsdefinierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuerelements zu sortieren. Der Index der einzelnen Elemente ändert sich entsprechend der neuen Sequenz. Sie können diese Nachricht explizit oder mithilfe des \_ SortItemsEx-Makros von ListView senden.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef492ff11980e764b33942f54c0732a64e799a94dde0e3d872ef0cb7bfb66c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170366"
---
# <a name="lvm_sortitemsex-message"></a>LVM \_ SORTITEMSEX-Nachricht

Verwendet eine anwendungsdefinierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuerelements zu sortieren. Der Index der einzelnen Elemente ändert sich entsprechend der neuen Sequenz. Sie können diese Nachricht explizit oder mithilfe des [**\_ SortItemsEx-Makros von ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anwendungsdefinierter Wert, der an die Vergleichsfunktion übergeben wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine anwendungsdefinierte Vergleichsfunktion. Sie wird während des Sortiervorgang jedes Mal aufgerufen, wenn die relative Reihenfolge von zwei Listenelementen verglichen werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die Vergleichsfunktion hat die folgende Form:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Diese Meldung ähnelt [**LVM \_ SORTITEMS,**](lvm-sortitems.md)mit Ausnahme des Informationstyps, der an die Vergleichsfunktion übergeben wird. Bei **LVM \_ SORTITEMSEX** ist *lParam1* der aktuelle Index des ersten Elements, und *lParam2* ist der aktuelle Index des zweiten Elements. Sie können eine [**LVM \_ GETITEMTEXT-Nachricht**](lvm-getitemtext.md) senden, um bei Bedarf weitere Informationen zu einem Element abzurufen.

Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element vor dem zweiten Element stehen soll, einen positiven Wert, wenn das erste Element dem zweiten element folgen soll, oder 0 (null), wenn die beiden Elemente gleichwertig sind.

> [!Note]  
> Während des Sortiervorgangs sind die Inhalte der Listenansicht instabil. Wenn die Rückruffunktion Nachrichten an das Listenansicht-Steuerelement sendet, abgesehen von [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GetItem),**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)sind die Ergebnisse unvorhersehbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





