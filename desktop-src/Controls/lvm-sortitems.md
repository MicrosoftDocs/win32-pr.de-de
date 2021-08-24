---
title: LVM_SORTITEMS (Commctrl.h)
description: Verwendet eine anwendungsdefinierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuerelements zu sortieren. Der Index der einzelnen Elemente ändert sich entsprechend der neuen Sequenz. Sie können diese Nachricht explizit oder mithilfe des \_ SortItems-Makros listview senden.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a245e8236995d0d595c339b322140ee53ab5f84e83f1ecbd6b8ed47293e7dc7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816390"
---
# <a name="lvm_sortitems-message"></a>LVM \_ SORTITEMS-Nachricht

Verwendet eine anwendungsdefinierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuerelements zu sortieren. Der Index der einzelnen Elemente ändert sich entsprechend der neuen Sequenz. Sie können diese Nachricht explizit oder mithilfe des [**\_ SortItems-Makros listview**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anwendungsdefinierter Wert, der an die Vergleichsfunktion übergeben wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die anwendungsdefinierte Vergleichsfunktion. Die Vergleichsfunktion wird während des Sortiervorgang jedes Mal aufgerufen, wenn die relative Reihenfolge von zwei Listenelementen verglichen werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die Vergleichsfunktion hat die folgende Form:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

Der *lParam1-Parameter* ist der Wert, der dem ersten verglichenen Element zugeordnet ist, und der *lParam2-Parameter* ist der Wert, der dem zweiten Element zugeordnet ist. Dies sind die Werte, die im **lParam-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) der Elemente angegeben wurden, als sie in die Liste eingefügt wurden. Der *wParam-Parameter* von [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)wird als dritter Parameter an die Rückruffunktion übergeben.

Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element vor dem zweiten Element stehen soll, einen positiven Wert, wenn das erste Element dem zweiten element folgen soll, oder 0 (null), wenn die beiden Elemente gleichwertig sind.

> [!Note]  
> Während des Sortiervorgangs sind die Inhalte der Listenansicht instabil. Wenn die Rückruffunktion Nachrichten an das Listenansicht-Steuerelement sendet, abgesehen von [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GetItem),**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)sind die Ergebnisse unvorhersehbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





