---
title: NM_TOOLTIPSCREATED Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35006c7c7f4cc66cc9ce5e387a362f423db43b6b7aab914d26360dd08d13b37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410313"
---
# <a name="nm_tooltipscreated-notification-code"></a>NM \_ TOOLTIPSCREATED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMTOOLTIPSCREATED-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Sofern nicht anders angegeben, ignoriert das Steuerelement den Rückgabewert aus diesem Benachrichtigungscode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





