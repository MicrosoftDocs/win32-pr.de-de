---
title: WM_CAP_SET_CALLBACK_WAVESTREAM (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM von Windows Multimedia
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
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622519"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM-Meldung

Die **MELDUNG WM CAP SET \_ \_ \_ CALLBACK \_ WAVESTREAM** legt eine Rückruffunktion in der Anwendung fest. AVICap ruft dieses Verfahren während der Streamingerfassung auf, wenn ein neuer Audiopuffer verfügbar wird. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) senden.


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Zeiger auf die Rückruffunktion des Wavestreams vom Typ [**capWaveStreamCallback.**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback) Geben **Sie NULL** für diesen Parameter an, um eine zuvor installierte Rückruffunktion für Wellenstreams zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **oder FALSE,** wenn die Streamingerfassung oder eine Einzelframe-Erfassungssitzung in Bearbeitung ist.

## <a name="remarks"></a>Hinweise

Das Erfassungsfenster ruft die Prozedur auf, bevor der Audiopuffer auf den Datenträger geschrieben wird. Dadurch können Anwendungen den Audiopuffer bei Wunsch ändern.

Wenn eine Wavestream-Rückruffunktion verwendet wird, muss sie installiert werden, bevor die Erfassungssitzung gestartet wird, und sie muss für die Dauer der Sitzung aktiviert bleiben. Sie kann nach dem Ende der Streamingerfassung deaktiviert werden.

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

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





