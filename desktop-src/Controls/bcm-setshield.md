---
title: BCM_SETSHIELD (Commctrl.h)
description: Legt den erforderlichen Höhe-Zustand für eine angegebene Schaltfläche oder einen Befehlslink fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des Button \_ SetElevationRequiredState-Makros.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD-Windows Steuerelemente
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ab7ab495e713d9f2c8d58c6723489f0099a7c2cba9df93d4f08870d521a0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921490"
---
# <a name="bcm_setshield-message"></a>BCM \_ SETSHIELD-Meldung

Legt den erforderlichen Höhe-Zustand für eine angegebene Schaltfläche oder einen Befehlslink fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des [**Button \_ SetElevationRequiredState-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Eine **BOOL,** die **TRUE ist,** um ein Symbol mit erhöhten Rechten zu zeichnen, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 1 oder andernfalls einen Fehlercode zurück.

## <a name="remarks"></a>Hinweise

Eine Anwendung muss für die Verwendung comctl32.dll Version 6 manifestiert werden, um diese Funktionalität nutzen zu können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





