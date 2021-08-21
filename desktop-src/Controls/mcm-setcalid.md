---
title: MCM_SETCALID (Commctrl.h)
description: Legt die Kalender-ID für das gegebene Kalendersteuer steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ SetCALID-Makros senden.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575580"
---
# <a name="mcm_setcalid-message"></a>MCM \_ SETCALID-Nachricht

Legt die Kalender-ID für das gegebene Kalendersteuer steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ SetCALID-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Kalender-ID. Eine der Calendar [Identifiers-Konstanten.](/windows/desktop/Intl/calendar-identifiers)

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

