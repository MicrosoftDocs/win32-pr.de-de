---
title: MCM_GETCALENDARCOUNT Meldung (Commctrl.h)
description: Ruft die Anzahl der Kalender ab, die derzeit im Kalendersteuerelement angezeigt werden. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetCalendarCount-Makros senden.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019048"
---
# <a name="mcm_getcalendarcount-message"></a>MCM \_ GETCALENDARCOUNT-Nachricht

Ruft die Anzahl der Kalender ab, die derzeit im Kalendersteuerelement angezeigt werden. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetCalendarCount-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anzahl von Kalendern, die derzeit im Kalendersteuerelement angezeigt werden. Die maximale Anzahl zulässiger Kalender beträgt 12.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





