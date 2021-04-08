---
title: LVM_SORTITEMS Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "mentems" senden.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Windows-Steuerelemente für LVM_SORTITEMS Meldung
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
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957265"
---
# <a name="lvm_sortitems-message"></a>LVM-Geräte \_ Nachricht

Verwendet eine Anwendungs definierte Vergleichsfunktion, um die Elemente eines Listenansicht-Steuer Elements zu sortieren. Der Index der einzelnen Elemente ändert sich, um die neue Sequenz widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**\_ mentems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der von der Anwendung definierte Wert, der an die Vergleichsfunktion übermittelt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die Anwendungs definierte Vergleichsfunktion. Die Vergleichsfunktion wird beim Sortiervorgang jedes Mal aufgerufen, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Vergleichsfunktion weist die folgende Form auf:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

Der *lParam1* -Parameter ist der Wert, der dem ersten zu vergleichenden Element zugeordnet ist, und der *lParam2* -Parameter ist der Wert, der dem zweiten Element zugeordnet ist. Dabei handelt es sich um die Werte, die im **LPARAM** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur der Elemente angegeben wurden, als Sie in die Liste eingefügt wurden. Der *wParam* -Parameter der [**\_ ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)-Elemente wird als dritter Parameter an die Rückruffunktion übergeben.

Die Vergleichsfunktion muss einen negativen Wert zurückgeben, wenn das erste Element dem zweiten vorangestellt wird, ein positiver Wert, wenn das erste Element der zweiten folgt, oder 0 (null), wenn die beiden Elemente äquivalent sind.

> [!Note]  
> Während des Sortier Vorgangs sind die Inhalte der Listenansicht instabil. Wenn die Rückruffunktion Nachrichten von [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) an das Listenansicht-Steuerelement sendet, sind die Ergebnisse unvorhersehbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





