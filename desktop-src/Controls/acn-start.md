---
title: ACN_START Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Animationssteuerelements, dass die Wiedergabe des zugeordneten AVI-Clips begonnen hat. Dieser Benachrichtigungscode wird in Form einer WM \_ COMMAND-Nachricht gesendet.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccfb5a1fc1f6b258cfe8363e99f38894ed7e601401d4f725431992a31f86376
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922160"
---
# <a name="acn_start-notification-code"></a>ACN \_ START-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Animationssteuerelements, dass die Wiedergabe des zugeordneten AVI-Clips begonnen hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet.


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Animationssteuerelements. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **HWND,** der das Handle für das Animationssteuerelement angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

