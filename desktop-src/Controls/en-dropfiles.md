---
title: EN_DROPFILES Benachrichtigungscode (Richedit.h)
description: Benachrichtigt ein übergeordnetes Fenster mit rich edit-Steuerelementen, dass der Benutzer versucht, Dateien in das Steuerelement zu löschen. Ein umfassendes Bearbeitungssteuersystem sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht, wenn es die WM \_ DROPFILES-Nachricht empfängt.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047780"
---
# <a name="en_dropfiles-notification-code"></a>EN \_ DROPFILES-Benachrichtigungscode

Benachrichtigt ein übergeordnetes Fenster mit rich edit-Steuerelementen, dass der Benutzer versucht, Dateien in das Steuerelement zu löschen. Ein umfassendes Bearbeitungssteuersystem sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht,**](wm-notify.md) wenn es die [**WM \_ DROPFILES-Nachricht empfängt.**](/windows/desktop/shell/wm-dropfiles)


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**ENDROPFILES-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) die gelöschte Dateien empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um den Abbruchvorgang zu ermöglichen.

Gibt 0 zurück, um den Abbruchvorgang zu ignorieren.

## <a name="remarks"></a>Hinweise

Damit ein umfassendes [**Bearbeitungssteuer steuerelement WM \_ DROPFILES-Nachrichten**](/windows/desktop/shell/wm-dropfiles) empfangen kann, muss das übergeordnete Fenster das Steuerelement mithilfe der [**DragAcceptFiles-Funktion**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) als Abbruchziel registrieren. Das Steuerelement registriert sich nicht selbst.

Um EN \_ DROPFILES-Benachrichtigungscodes zu erhalten, geben Sie [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.

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

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

