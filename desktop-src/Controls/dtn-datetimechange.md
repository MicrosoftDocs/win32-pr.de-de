---
title: DTN_DATETIMECHANGE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be916859a8c963c81d1f68410e9e821c430832610aa85378a6ae6162e0488bf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877700"
---
# <a name="dtn_datetimechange-notification-code"></a>DTN \_ DATETIMECHANGE-Benachrichtigungscode

Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMECHANGE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) die Informationen über die Änderung enthält, die im -Steuerelement stattgefunden hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuerelements muss 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





