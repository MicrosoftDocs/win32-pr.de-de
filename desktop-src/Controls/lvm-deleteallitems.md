---
title: LVM_DELETEALLITEMS Meldung (Commctrl.h)
description: Entfernt alle Elemente aus einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteAllItems-Makros senden.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958409"
---
# <a name="lvm_deleteallitems-message"></a>LVM \_ DELETEALLITEMS-Nachricht

Entfernt alle Elemente aus einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteAllItems-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn ein Listenansichtssteuerelement die **LVM \_ DELETEALLITEMS-Nachricht** empfängt, sendet es den [**LVN \_ DELETEALLITEMS-Benachrichtigungscode**](lvn-deleteallitems.md) an das übergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





