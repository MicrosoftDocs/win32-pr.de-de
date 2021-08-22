---
title: EN_CORRECTTEXT Benachrichtigungscode (Richedit.h)
description: Benachrichtigt ein übergeordnetes Fenster mit rich edit-Steuerelement, dass eine SYV CORRECT-Geste aufgetreten ist, was dem übergeordneten Fenster die Möglichkeit gibt, die Textbearbeitung \_ abzubricht. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019418"
---
# <a name="en_correcttext-notification-code"></a>EN \_ CORRECTTEXT-Benachrichtigungscode

Benachrichtigt ein übergeordnetes Fenster mit rich edit-Steuerelement, dass eine SYV CORRECT-Geste aufgetreten ist, was dem übergeordneten Fenster die Möglichkeit gibt, die Textbearbeitung \_ abzubricht. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**ENCORRECTTEXT-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) die die zu korrigierende Auswahl an gibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, um die Aktion zu ignorieren.

Gibt einen Wert ungleich 0 (null) zurück, um die Aktion zu verarbeiten.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nur gesendet, wenn Stiftfunktionen verfügbar sind.

Um EN \_ CORRECTTEXT-Benachrichtigungscodes zu erhalten, geben Sie [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.

> [!Note]  
> Der EN \_ CORRECTTEXT-Benachrichtigungscode wird nur in Rich-Edit-Version 1.0 unterstützt. Sie wird in späteren Versionen von Rich Edit nicht unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





