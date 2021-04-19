---
title: WM_CAP_SET_CALLBACK_FRAME Meldung (VFW. h)
description: Die \_ Rückruffunktion für den WM-Cap- \_ Satz \_ \_ legt eine Vorschau Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn das Aufzeichnungs Fenster vorschauframes erfasst. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonframe-Makros senden.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337937"
---
# <a name="wm_cap_set_callback_frame-message"></a>\_ \_ \_ Rückruf \_ Rahmen Nachricht für WM-Cap-Satz

Die Rückruffunktion für den WM-Cap-Satz legt eine Vorschau Rückruffunktion in der Anwendung **\_ \_ fest \_ \_** . Avicap ruft dieses Verfahren auf, wenn das Aufzeichnungs Fenster vorschauframes erfasst. Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonframe**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) -Makros senden.


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*
</dt> <dd>

Zeiger auf die Vorschau Rückruffunktion vom Typ [**capvideostreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Das Erfassungsfenster Ruft die Rückruffunktion auf, bevor Vorschau Frames angezeigt werden. Dies ermöglicht es einer Anwendung, den Frame bei Bedarf zu ändern. Diese Rückruffunktion wird bei der Streaming-Video Erfassung nicht verwendet.

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

 

 





