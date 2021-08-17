---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM (Vfw.h)
description: Die WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM-Nachricht legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM von Windows Multimedia
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
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940718"
---
# <a name="wm_cap_set_callback_videostream-message"></a>WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM-Meldung

Die **WM CAP SET \_ \_ \_ CALLBACK \_ VIDEOSTREAM-Nachricht** legt eine Rückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren während der Streamingerfassung auf, wenn ein Videopuffer gefüllt wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) senden.


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Videostream-Rückruffunktion vom Typ [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Geben **Sie NULL** für diesen Parameter an, um eine zuvor installierte Videostream-Rückruffunktion zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **oder FALSE,** wenn streaming capture oder eine Singleframe-Erfassungssitzung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

Das Erfassungsfenster ruft die Rückruffunktion auf, bevor der erfasste Frame auf den Datenträger geschrieben wird. Dadurch können Anwendungen den Frame bei Wunsch ändern.

Wenn eine Videostream-Rückruffunktion für streaming capture verwendet wird, muss die Prozedur vor dem Starten der Erfassungssitzung installiert werden und für die Dauer der Sitzung aktiviert bleiben. Sie kann nach dem Ende der Streamingerfassung deaktiviert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





