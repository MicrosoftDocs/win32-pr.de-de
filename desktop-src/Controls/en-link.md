---
title: EN_LINK Benachrichtigungscode (Richedit.h)
description: Ein Rich-Edit-Steuerelement sendet EN \_ LINK-Benachrichtigungscodes, wenn es verschiedene Nachrichten empfängt, z. B. wenn der Benutzer mit der Maus klickt oder wenn sich der Mauszeiger über Text befindet, der den \_ CFE LINK-Effekt hat.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3398f79a94982a8b7c843747f38f16431cad6a061388367037d259cfe862d468
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047660"
---
# <a name="en_link-notification-code"></a>EN \_ LINK-Benachrichtigungscode

Ein Rich-Edit-Steuerelement sendet EN \_ LINK-Benachrichtigungscodes, wenn es verschiedene Nachrichten empfängt, z. B. wenn der Benutzer mit der Maus klickt oder wenn sich der Mauszeiger über Text befindet, der den **CFE \_ LINK-Effekt** hat. Ein fensterloses Rich Edit-Steuerelement sendet diese Benachrichtigung mithilfe der [**ITextHost::TxNotify-Methode.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ NOTIFY-Meldung.**](wm-notify.md)


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Fenster-ID, die durch Aufrufen der [**GetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) mit dem \_ GWL-ID-Wert abgerufen wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ENLINK-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-enlink) Die -Struktur enthält eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) Informationen zum Benachrichtigungscode und eine [**CHARRANGE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-charrange) die den Zeichenbereich angibt, der den **CFE \_ LINK-Effekt** aufweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit das Steuerelement mit der normalen Verarbeitung der Nachricht fortfahren kann.

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement die Nachricht verarbeitet.

**Windows 8:** Geben Sie **EN \_ LINK DO \_ \_ DEFAULT** zurück, um das Rich Edit-Steuerelement anweisen, die Standardaktion auszuführen.

## <a name="remarks"></a>Hinweise

Um **EN \_ LINK-Benachrichtigungscodes** zu erhalten, wenn der Link den Fokus besitzt, geben Sie das [**ENM \_ LINK-Flag**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

Wenn der Link keinen Fokus besitzt, geben Sie zum Empfangen von **EN \_ LINK-Benachrichtigungscodes** das **Flag SES \_ NOFOCUSLINKNOTIFY** in der Maske an, die mit der [**EM \_ SETEDITSTYLE-Nachricht**](em-seteditstyle.md) gesendet wird.

Ein Rich-Edit-Steuerelement sendet **EN LINK-Benachrichtigungscodes, \_** wenn es die folgenden Nachrichten empfängt, während sich der Mauszeiger über Text befindet, der den **CFE \_ LINK-Effekt** hat:

-   [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ RBUTTONDBLCLK**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)

Der **CFE \_ LINK-Effekt** identifiziert in der Regel einen Textbereich, der eine URL enthält. Anwendungen können den \_ EN LINK-Benachrichtigungscode verarbeiten, indem sie den Mauszeiger ändern, wenn er sich über der URL befindet, oder indem sie einen Browser starten, um den durch die URL identifizierten Speicherort anzuzeigen.

Wenn Sie die [**EM \_ AUTOURLDETECT-Nachricht**](em-autourldetect.md) senden, um die automatische URL-Erkennung zu aktivieren, legt das Rich Edit-Steuerelement automatisch den **CFE \_ LINK-Effekt** für geänderten Text fest, der als URL identifiziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2::SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

