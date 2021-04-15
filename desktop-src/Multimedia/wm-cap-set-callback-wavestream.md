---
title: WM_CAP_SET_CALLBACK_WAVESTREAM Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Callback \_ WaveStream"-Nachricht legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479056"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>WM- \_ Cap- \_ Rückruf- \_ \_ WaveStream-Nachricht

Die " **WM \_ Cap \_ Set \_ Callback \_ WaveStream** "-Nachricht legt eine Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren während der streamingerfassung auf, wenn ein neuer Audiopuffer verfügbar wird. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonwavestream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Ein Zeiger auf die Funktion "Wave Stream Callback" vom Typ [**capwavestreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Wave Stream-Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Im Fenster erfassen wird die Prozedur aufgerufen, bevor der Audiopuffer auf den Datenträger geschrieben wird. Dies ermöglicht es Anwendungen, den Audiopuffer bei Bedarf zu ändern.

Wenn eine Wave Stream-Rückruffunktion verwendet wird, muss Sie vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben. Sie kann nach Ende der streamingerfassung deaktiviert werden.

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

 

 





