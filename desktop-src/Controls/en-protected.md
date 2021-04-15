---
title: EN_PROTECTED Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer eine Aktion durchführt, die einen geschützten Textbereich ändert. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- Windows-Steuerelemente für EN_PROTECTED Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476977"
---
# <a name="en_protected-notification-code"></a>EN \_ geschützter Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer eine Aktion durchführt, die einen geschützten Textbereich ändert. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**geschützte**](/windows/desktop/api/Richedit/ns-richedit-enprotected) Struktur, die Informationen über die Meldung enthält, die den Benachrichtigungs Code ausgelöst hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, um den Vorgang zuzulassen.

Gibt einen Wert ungleich 0 zurück, um den Vorgang zu verhindern.

## <a name="remarks"></a>Bemerkungen

Wenn 0 (null) zurückgegeben wird und die Member " **msg**", " **wParam**" und " **LPARAM** " der [**geschützten**](/windows/desktop/api/Richedit/ns-richedit-enprotected) Struktur geändert werden, verarbeitet das Steuerelement die überarbeitete Nachricht anstelle der ursprünglichen Nachricht.

Um \_ geschützte Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ Protected**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.

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

[**Geschützt**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





