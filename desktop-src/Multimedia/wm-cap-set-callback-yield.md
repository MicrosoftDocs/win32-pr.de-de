---
title: WM_CAP_SET_CALLBACK_YIELD-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SET \_ CALLBACK \_ YIELD-Nachricht legt eine Rückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der Streamingerfassung ergibt. Sie können diese Nachricht explizit oder mithilfe des Makros capSetCallbackOnYield senden.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD nachricht Windows Multimedia
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
ms.openlocfilehash: ee12db79a9e4808442618ca295694611aa9e098a87c8f72b25f04360e156c8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622235"
---
# <a name="wm_cap_set_callback_yield-message"></a>MELDUNG "WM \_ CAP \_ SET \_ CALLBACK \_ YIELD"

Die **WM CAP SET \_ \_ \_ CALLBACK \_ YIELD-Nachricht** legt eine Rückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren auf, wenn das Erfassungsfenster während der Streamingerfassung ergibt. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) senden.


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Yield-Rückruffunktion vom Typ [**capYieldCallback.**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback) Geben Sie **NULL** für diesen Parameter an, um eine zuvor installierte Yield-Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn die Streamingerfassung oder eine Singleframe-Erfassungssitzung ausgeführt wird.

## <a name="remarks"></a>Hinweise

Anwendungen können optional eine Yield-Rückruffunktion festlegen. Die Yield-Rückruffunktion wird mindestens einmal für jeden Videoframe aufgerufen, der während der Streamingerfassung erfasst wurde. Wenn eine Yield-Rückruffunktion installiert ist, wird sie unabhängig vom Zustand des **fYield-Members** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) aufgerufen.

Wenn die Yield-Rückruffunktion verwendet wird, muss sie vor dem Starten der Aufzeichnungssitzung installiert und für die Dauer der Sitzung aktiviert bleiben. Sie kann deaktiviert werden, nachdem die Streamingerfassung beendet wurde.

Anwendungen führen in der Regel eine Art von Nachrichtenverarbeitung in der Rückruffunktion durch, die aus einer [PeekMessage-,](/windows/win32/api/winuser/nf-winuser-peekmessagea) [TranslateMessage-](/windows/win32/api/winuser/nf-winuser-translatemessage)und [DispatchMessage-Schleife](/windows/win32/api/winuser/nf-winuser-dispatchmessage) besteht, wie in der Nachrichtenschleife einer [WinMain-Funktion.](/windows/win32/api/winbase/nf-winbase-winmain) Die Yield-Rückruffunktion muss auch Nachrichten filtern und entfernen, die Wiederinvarianzprobleme verursachen können.

Eine Anwendung gibt in der Regel **TRUE** in der Yield-Prozedur zurück, um die Streamingerfassung fortzusetzen. Wenn eine Yield-Rückruffunktion **FALSE** zurückgibt, beendet das Erfassungsfenster den Erfassungsprozess.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

