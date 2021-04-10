---
title: LVM_SORTITEMSEX Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "mentemsex" senden.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Windows-Steuerelemente für LVM_SORTITEMSEX Meldung
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
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040175"
---
# <a name="lvm_sortitemsex-message"></a>LVM- \_ Nachricht

Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**\_ mentemsex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der von der Anwendung definierte Wert, der an die Vergleichsfunktion übermittelt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine Anwendungs definierte Vergleichsfunktion. Sie wird während des Sortier Vorgangs jedes Mal aufgerufen, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Vergleichsfunktion weist die folgende Form auf:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Diese Meldung ähnelt LVM- [**Elementen \_**](lvm-sortitems.md), mit Ausnahme der Art von Informationen, die an die Vergleichsfunktion übermittelt werden. Mit **LVM \_**-Element-Sexualität ist *lParam1* der aktuelle Index des ersten Elements, und *lParam2* ist der aktuelle Index des zweiten Elements. Wenn erforderlich, können Sie eine [**LVM- \_ GetItemText**](lvm-getitemtext.md) -Nachricht senden, um weitere Informationen zu einem Element abzurufen.

Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element dem zweiten vorangestellt wird, ein positiver Wert, wenn das erste Element der zweiten folgt, oder 0 (null), wenn die beiden Elemente äquivalent sind.

> [!Note]  
> Während des Sortier Vorgangs sind die Inhalte der Listenansicht instabil. Wenn die Rückruffunktion Nachrichten von [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) an das Listenansicht-Steuerelement sendet, sind die Ergebnisse unvorhersehbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





