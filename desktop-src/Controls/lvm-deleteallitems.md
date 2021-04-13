---
title: LVM_DELETEALLITEMS Meldung (kommstrg. h)
description: Entfernt alle Elemente aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteAllItems-Makros senden.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Windows-Steuerelemente für LVM_DELETEALLITEMS Meldung
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
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475201"
---
# <a name="lvm_deleteallitems-message"></a>LVM \_ DeleteAllItems-Meldung

Entfernt alle Elemente aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn ein Listenansicht-Steuerelement die **LVM- \_ DeleteAllItems** -Nachricht empfängt, sendet es den [**LVN \_ DeleteAllItems**](lvn-deleteallitems.md) -Benachrichtigungs Code an das übergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





