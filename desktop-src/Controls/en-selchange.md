---
title: EN_SELCHANGE Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass sich die aktuelle Auswahl geändert hat. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a2398abd5058f57eeef6ad73f559a723e7df29315d38dfc9794a707740c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047420"
---
# <a name="en_selchange-notification-code"></a>EN \_ SELCHANGE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass sich die aktuelle Auswahl geändert hat. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**SELCHANGE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-selchange) die Informationen zur Auswahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um EN \_ SELCHANGE-Benachrichtigungscodes zu empfangen, geben Sie [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

Dieser Benachrichtigungscode wird gesendet, wenn sich die Position des Caretzeichens ändert und kein Text ausgewählt wird (die Auswahl ist leer). Die Caretposition kann sich ändern, wenn der Benutzer mit der Maus klickt, eine Pfeiltaste eingibt oder drückt.

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





