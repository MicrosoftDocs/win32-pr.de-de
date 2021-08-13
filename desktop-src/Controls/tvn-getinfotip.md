---
title: TVN_GETINFOTIP Benachrichtigungscode (Commctrl.h)
description: Wird von einem Strukturansicht-Steuerelement gesendet, das über den TVS \_ INFOTIP-Stil verfügt. Dieser Benachrichtigungscode wird gesendet, wenn das Steuerelement zusätzliche Textinformationen an fordert, die in einer QuickInfo angezeigt werden sollen. Der Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5129e1fa97397cfa9c037c7c65099ee3bd961f184b1bf9b43d2dc87e35880f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261160"
---
# <a name="tvn_getinfotip-notification-code"></a>TVN \_ GETINFOTIP-Benachrichtigungscode

Wird von einem Strukturansicht-Steuerelement gesendet, das über den [**TVS \_ INFOTIP-Stil**](tree-view-control-window-styles.md) verfügt. Dieser Benachrichtigungscode wird gesendet, wenn das Steuerelement zusätzliche Textinformationen an fordert, die in einer QuickInfo angezeigt werden sollen. Der Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVGETINFOTIP-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) die Informationen zu diesem Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das -Steuerelement ignoriert den Rückgabewert für diesen Benachrichtigungscode.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nur von Strukturansichtssteuerelementen gesendet, die den [**TVS \_ INFOTIP-Stil**](tree-view-control-window-styles.md) haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ GETINFOTIPW** (Unicode) und **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





