---
title: EN_SELCHANGE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass sich die aktuelle Auswahl geändert hat. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- Windows-Steuerelemente für EN_SELCHANGE Benachrichtigungs
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
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743032"
---
# <a name="en_selchange-notification-code"></a>EN \_ selChange-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass sich die aktuelle Auswahl geändert hat. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) -Struktur, die Informationen über die Auswahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um en \_ selChange-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Abmeldung gesendet wird.

Dieser Benachrichtigungs Code wird gesendet, wenn sich die Position der Einfügemarke ändert und kein Text ausgewählt ist (die Auswahl ist leer). Die Position der Einfügemarke kann sich ändern, wenn der Benutzer auf die Maus, die Typen klickt oder eine Pfeiltaste drückt.

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

[**SelChange**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





