---
title: EN_MSGFILTER Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements über ein Tastatur- oder Mausereignis im Steuerelement. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d2cbe47af3d74deb4795946d58871b4729118db0e839027e78e05976ebf855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436710"
---
# <a name="en_msgfilter-notification-code"></a>EN \_ MSGFILTER-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements über ein Tastatur- oder Mausereignis im Steuerelement. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**MSGFILTER-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) die Informationen zur Tastatur- oder Mausmeldung enthält. Wenn das übergeordnete Fenster diese Struktur ändert und einen Wert ungleich 0 (null) zurückgibt, wird die geänderte Nachricht anstelle der ursprünglichen verarbeitet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn das Steuerelement das Tastatur- oder Mausereignis verarbeiten soll.

Gibt einen Anderen als 0 (null) zurück, wenn das Steuerelement das Tastatur- oder Mausereignis ignorieren soll.

## <a name="remarks"></a>Hinweise

Um EN MSGFILTER-Benachrichtigungscodes für Ereignisse zu empfangen, geben Sie mindestens eines der folgenden Flags in der Maske an, die mit der \_ [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.



| Flag                                                                             | Bedeutung                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | Zum Empfangen von Benachrichtigungscodes für Tastaturereignisse.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Zum Empfangen von Benachrichtigungscodes für Mausereignisse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Zum Empfangen von Benachrichtigungscodes für ein Mausradereignis. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





