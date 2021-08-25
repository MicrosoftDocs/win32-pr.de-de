---
title: NM_THEMECHANGED Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass sich das Design geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069f4eb2b3727edc19c531f4404b723df2ea775677a25283268c1c20a978dedc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877260"
---
# <a name="nm_themechanged-notification-code"></a>NM \_ THEMECHANGED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass sich das Design geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom -Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





