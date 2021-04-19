---
title: WM_CAP_SET_CALLBACK_YIELD Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set Callback yield"- \_ \_ Nachricht legt eine Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der streamingerfassung ergibt. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonyield-Makros senden.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337903"
---
# <a name="wm_cap_set_callback_yield-message"></a>Zurück \_ gebende \_ \_ Rückruf \_ Meldung für die WM-Abdeckung

Die " **WM \_ Cap \_ Set \_ Callback \_ Yield** "-Nachricht legt eine Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der streamingerfassung ergibt. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonyield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Ein Zeiger auf die Yield Callback-Funktion vom Typ [**capyieldcallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Yield-Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Anwendungen können optional eine Yield-Rückruffunktion festlegen. Die Yield Callback-Funktion wird für jeden Video Frame, der während der streamingerfassung aufgezeichnet wurde, mindestens einmal aufgerufen. Wenn eine Yield Callback-Funktion installiert ist, wird Sie unabhängig vom Zustand des **fyield** -Members der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur aufgerufen.

Wenn die Yield Callback-Funktion verwendet wird, muss Sie vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben. Sie kann nach Ende der streamingerfassung deaktiviert werden.

Anwendungen führen in der Regel eine Art der Nachrichtenverarbeitung in der Rückruffunktion aus, die aus einer " [Peer-Message](/windows/win32/api/winuser/nf-winuser-peekmessagea)", " [translatemess Age](/windows/win32/api/winuser/nf-winuser-translatemessage)" und " [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) "-Schleife besteht, wie in der Nachrichten Schleife einer [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion. Die Yield Callback-Funktion muss auch Nachrichten filtern und entfernen, die Probleme bei der Wiedereintritts Fähigkeit verursachen können.

Eine Anwendung gibt in der Regel " **true** " zurück, um die streamingerfassung fortzusetzen. Wenn eine Yield Callback-Funktion **false** zurückgibt, hält das Erfassungsfenster den Erfassungsprozess an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

