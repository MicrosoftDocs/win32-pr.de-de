---
title: MCN_VIEWCHANGE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn sich die aktuelle Ansicht ändert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef04fc370d67f6e6c7a4ef854d542584e170ddd05bf7c12a5135c84e97f33875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799130"
---
# <a name="mcn_viewchange-notification-code"></a>MCN \_ VIEWCHANGE-Benachrichtigungscode

Wird von einem Monatskalender-Steuerelement gesendet, wenn sich die aktuelle Ansicht ändert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMVIEWCHANGE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) die Informationen zur aktuellen Ansicht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





