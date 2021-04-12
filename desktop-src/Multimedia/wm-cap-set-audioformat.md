---
title: WM_CAP_SET_AUDIOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Audioformat"-Meldung legt das Audioformat fest, das beim Ausführen von Streaming oder Schritt Erfassung verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des capsetaudioformat-Makros senden.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104151"
---
# <a name="wm_cap_set_audioformat-message"></a>WM \_ Cap \_ Set \_ Audioformat-Meldung

Die " **WM \_ Cap \_ Set \_ Audioformat** "-Meldung legt das Audioformat fest, das beim Ausführen von Streaming oder Schritt Erfassung verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des [**capsetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) -Makros senden.


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psaudioformat*
</dt> <dd>

Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -oder [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Struktur, die das Audioformat definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

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

 

