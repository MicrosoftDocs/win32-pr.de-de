---
title: LVM_ISITEMVISIBLE (Commctrl.h)
description: Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ IsItemVisible-Makros.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE meldungssteuerelemente Windows
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
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958179"
---
# <a name="lvm_isitemvisible-message"></a>LVM \_ ISITEMVISIBLE-Nachricht

Gibt an, ob ein Element im Listenansicht-Steuerelement sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ IsItemVisible-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Index des Elements im Listenansicht-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn sichtbar, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





