---
title: MCN_GETDAYSTATE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, um Informationen über die Anzeige einzelner Tage anzufordern. Dieser Benachrichtigungs Code wird nur nach Monatskalender-Steuerelementen gesendet, die den MCS \_ daystate-Stil verwenden, und er wird in Form einer WM- \_ Benachrichtigungs Meldung gesendet.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- Windows-Steuerelemente für MCN_GETDAYSTATE Benachrichtigungs
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
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741689"
---
# <a name="mcn_getdaystate-notification-code"></a>MCN \_ getdaystate-Benachrichtigungs Code

Wird von einem Monatskalender-Steuerelement gesendet, um Informationen über die Anzeige einzelner Tage anzufordern. Dieser Benachrichtigungs Code wird nur nach Monatskalender-Steuerelementen gesendet, die den [**MCS \_ daystate**](month-calendar-control-styles.md) -Stil verwenden, und er wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmdaystate**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) -Struktur. Die Struktur enthält Informationen über den Zeitraum, für den das Steuerelement Informationen benötigt, und empfängt die Adresse eines Arrays, das diese Daten bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Durch die Behandlung dieses Benachrichtigungs Codes kann Ihre Anwendung Ihre Anzeige anpassen, indem Sie angeben, dass bestimmte Tage fett angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





