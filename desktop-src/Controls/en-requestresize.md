---
title: EN_REQUESTRESIZE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Inhalt des Steuer Elements entweder kleiner oder größer als die Fenstergröße des Steuer Elements ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Windows-Steuerelemente für EN_REQUESTRESIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104498"
---
# <a name="en_requestresize-notification-code"></a>EN \_ RequestResize-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Inhalt des Steuer Elements entweder kleiner oder größer als die Fenstergröße des Steuer Elements ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**reqresize**](/windows/desktop/api/Richedit/ns-richedit-reqresize) -Struktur, die die angeforderte Größe empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um das Verhalten eines Rich-Edit-Steuer Elements zu unterstützen, muss das übergeordnete Fenster die Größe des Steuer Elements ändern, wenn es diesen Benachrichtigungs Code empfängt.

Zum Empfangen von en \_ RequestResize-Benachrichtigungs Codes geben Sie [**ENM \_ RequestResize**](rich-edit-control-event-mask-flags.md) in der mit der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) gesendeten Maske an.

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

[**Reqresize**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





