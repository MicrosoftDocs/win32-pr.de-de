---
title: LVM_ISITEMVISIBLE Meldung (kommstrg. h)
description: Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des ListView-Objekts \_ isitemvisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Windows-Steuerelemente für LVM_ISITEMVISIBLE Meldung
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859148"
---
# <a name="lvm_isitemvisible-message"></a>LVM- \_ isitemvisible-Meldung

Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView-Objekts \_ isitemvisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Index des Elements im Listenansicht-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn es sichtbar ist, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





