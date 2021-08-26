---
title: EN_REQUESTRESIZE Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass der Inhalt des Steuerelements entweder kleiner oder größer als die Fenstergröße des Steuerelements ist. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE Benachrichtigungscode Windows Controls
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
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047580"
---
# <a name="en_requestresize-notification-code"></a>EN \_ REQUESTRESIZE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass der Inhalt des Steuerelements entweder kleiner oder größer als die Fenstergröße des Steuerelements ist. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**REQRESIZE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-reqresize) die die angeforderte Größe empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um das bottomless-Verhalten eines Rich-Edit-Steuerelements zu unterstützen, muss das übergeordnete Fenster die Größe des Steuerelements ändern, wenn es diesen Benachrichtigungscode empfängt.

Um EN \_ REQUESTRESIZE-Benachrichtigungscodes zu empfangen, geben Sie [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





