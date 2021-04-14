---
title: EN_LINK Benachrichtigungs Code (RichEdit. h)
description: Ein RichEdit-Steuerelement sendet \_ beim empfangen verschiedener Nachrichten eine Eingabe-/Link-Benachrichtigung, z. b. wenn der Benutzer auf die Maus klickt oder wenn sich der Mauszeiger über dem Text befindet, der den CFE- \_ Link Effekt aufweist.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- Windows-Steuerelemente für EN_LINK Benachrichtigungs
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
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478555"
---
# <a name="en_link-notification-code"></a>EN \_ Link-Benachrichtigungs Code

Ein RichEdit-Steuerelement sendet \_ beim empfangen verschiedener Nachrichten eine Eingabe-/Link-Benachrichtigung, z. b. wenn der Benutzer auf die Maus klickt oder wenn sich der Mauszeiger über dem Text befindet, der den **CFE- \_ Link** Effekt aufweist. Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der [**itexthost:: txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode gesendet. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Fenster-ID, die durch Aufrufen der [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-ID-Wert abgerufen wird \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**einlinkstruktur**](/windows/desktop/api/Richedit/ns-richedit-enlink) . Die Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, Informationen über den Benachrichtigungs Code und eine [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur, die den Zeichenbereich angibt, der den **CFE- \_ Link** Effekt aufweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, damit das Steuerelement mit der normalen Verarbeitung der Nachricht fortfahren kann.

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement die Meldung

**Windows 8**: Rückgabe- **de- \_ Link \_ \_ standardmäßig** wird das Rich Edit-Steuerelement zum Ausführen der Standardaktion angewiesen.

## <a name="remarks"></a>Bemerkungen

Geben Sie das [**ENM- \_ linkflag**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht " [**EM \_ SetEventMask**](em-seteventmask.md) " gesendet wird, um die Verbindungs Benachrichtigungs Codes von **en \_** zu erhalten

Wenn der Link keinen Fokus hat, geben Sie zum Empfangen von **en- \_ Link** -Benachrichtigungs Codes das **SES \_ nofocuslinklotify** -Flag in der Maske an, die mit der [**EM \_ setEditStyle**](em-seteditstyle.md) -Nachricht gesendet wurde.

Ein Rich-Edit-Steuerelement sendet beim Empfang der folgenden Meldungen die beim **empfangen der folgenden \_** Meldungen gesendeten **\_ Verbindungs** Benachrichtigungs Codes:

-   [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM- \_ mouseelmove**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM- \_ rbuttondblclk**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM- \_ rbuttondown**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor)

Der **CFE- \_ Link** Effekt identifiziert in der Regel einen Textbereich, der eine URL enthält. Anwendungen können den e- \_ Link-Benachrichtigungs Code verarbeiten, indem Sie den Mauszeiger ändern, wenn er sich über der URL befindet, oder indem Sie einen Browser starten, um den von der URL identifizierten Speicherort anzuzeigen.

Wenn Sie die [**EM \_ autourldetect**](em-autourldetect.md) -Nachricht senden, um die automatische URL-Erkennung zu aktivieren, legt das Rich Edit-Steuerelement automatisch den **CFE- \_ Link** Effekt für geänderten Text fest, der als URL identifiziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeichenbereich**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ autourldetect**](em-autourldetect.md)
</dt> <dt>

[**Verknüpfen**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2:: tarturl**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

