---
title: EN_MSGFILTER Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements über ein Tastatur-oder Maus Ereignis im-Steuerelement. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- Windows-Steuerelemente für EN_MSGFILTER Benachrichtigungs
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
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103929"
---
# <a name="en_msgfilter-notification-code"></a>EN \_ msgfilter-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements über ein Tastatur-oder Maus Ereignis im-Steuerelement. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) -Struktur, die Informationen über die Tastatur-oder Maus Meldung enthält. Wenn das übergeordnete Fenster diese Struktur ändert und einen Wert ungleich 0 (null) zurückgibt, wird die geänderte Nachricht anstelle der ursprünglichen verarbeitet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, wenn das Steuerelement das Tastatur-oder Maus Ereignis verarbeiten soll.

Gibt einen Wert ungleich 0 zurück, wenn das Steuerelement das Tastatur-oder Maus Ereignis ignorieren soll.

## <a name="remarks"></a>Bemerkungen

Zum Empfangen von en- \_ msgfilter-Benachrichtigungs Codes für Ereignisse geben Sie mindestens eines der folgenden Flags in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht "-Abmeldung gesendet" gesendet wird.



| Flag                                                                             | Bedeutung                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**"ESM"- \_ KEYEVENTs**](rich-edit-control-event-mask-flags.md)       | Zum Empfangen von Benachrichtigungs Codes für Tastatur Ereignisse.     |
| [**"en"- \_ mouevent-Ereignisse**](rich-edit-control-event-mask-flags.md)   | Zum Empfangen von Benachrichtigungs Codes für Mausereignisse.        |
| [**\_SM-scrollevents**](rich-edit-control-event-mask-flags.md) | Zum Empfangen von Benachrichtigungs Codes für ein Mausrad Ereignis. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





