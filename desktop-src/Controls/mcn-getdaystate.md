---
title: MCN_GETDAYSTATE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Monatskalender-Steuerelement gesendet, um Informationen darüber an fordern, wie einzelne Tage angezeigt werden sollen. Dieser Benachrichtigungscode wird nur von Monatskalender-Steuerelementen gesendet, die den MCS DAYSTATE-Stil verwenden, und in Form einer \_ WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64af64fde86ed91ae41cbd3fed53e9cb27a0be410140bc1d25e0548a64042668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697140"
---
# <a name="mcn_getdaystate-notification-code"></a>MCN \_ GETDAYSTATE-Benachrichtigungscode

Wird von einem Monatskalender-Steuerelement gesendet, um Informationen darüber an fordern, wie einzelne Tage angezeigt werden sollen. Dieser Benachrichtigungscode wird nur von Monatskalender-Steuerelementen gesendet, die den [**MCS \_ DAYSTATE-Stil**](month-calendar-control-styles.md) verwenden, und in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMDAYSTATE-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) Die -Struktur enthält Informationen über den Zeitrahmen, für den das Steuerelement Informationen benötigt, und empfängt die Adresse eines Arrays, das diese Daten zur Verfügung stellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Durch die Verarbeitung dieses Benachrichtigungscodes kann Ihre Anwendung die Anzeige anpassen, indem sie an, dass bestimmte Tage fett angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





