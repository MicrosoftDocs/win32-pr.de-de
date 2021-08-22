---
title: WM_CAP_GET_AUDIOFORMAT Nachricht (Vfw.h)
description: Die WM \_ CAP \_ GET \_ AUDIOFORMAT-Nachricht ruft das Audioformat oder die Größe des Audioformats ab. Sie können diese Nachricht explizit oder mithilfe der Makros capGetAudioFormat und capGetAudioFormatSize senden.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d247c035f251b387537f8e6c360adf79e6ed479d8d40e4f8fe8180e059dab3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940738"
---
# <a name="wm_cap_get_audioformat-message"></a>WM \_ CAP \_ GET \_ AUDIOFORMAT-Nachricht

Die **WM CAP GET \_ \_ \_ AUDIOFORMAT-Nachricht** ruft das Audioformat oder die Größe des Audioformats ab. Sie können diese Nachricht explizit oder mithilfe der Makros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) senden.


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

Zeiger auf eine [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) oder **NULL.** Wenn der Wert **NULL** ist, wird die Größe in Bytes zurückgegeben, die zum Speichern der -Struktur erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe des Audioformats in Bytes zurück.

## <a name="remarks"></a>Hinweise

Da komprimierte Audioformate in den Größenanforderungen variieren, müssen Anwendungen zuerst die Größe abrufen, dann Speicher belegen und schließlich die Audioformatdaten anfordern.

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

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

