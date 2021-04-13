---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Callback Videostream"- \_ Meldung legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391544"
---
# <a name="wm_cap_set_callback_videostream-message"></a>WM- \_ Cap- \_ Rückruf- \_ \_ videostreamnachricht

Die " **WM \_ Cap \_ Set \_ Callback \_ Videostream** "-Meldung legt eine Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren während der streamingerfassung auf, wenn ein Video Puffer gefüllt wird. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonvideostream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Ein Zeiger auf die videostreamrückruf-Funktion vom Typ [**capvideostreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte videostreamrückruf-Funktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Das Aufzeichnungs Fenster Ruft die Rückruffunktion auf, bevor der erfasste Frame auf den Datenträger geschrieben wird. Dies ermöglicht es Anwendungen, den Frame bei Bedarf zu ändern.

Wenn eine videostreamrückruf-Funktion für die streamingerfassung verwendet wird, muss die Prozedur vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben. Sie kann nach Ende der streamingerfassung deaktiviert werden.

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

 

 





