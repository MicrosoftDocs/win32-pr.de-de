---
title: WM_CAP_GET_AUDIOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ get \_ Audioformat"-Nachricht erhält das Audioformat oder die Größe des Audioformats. Sie können diese Nachricht explizit oder mithilfe der Makros capgetaudioformat und capgetaudioformatsize senden.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT-Nachricht (Multimedia)
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
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391506"
---
# <a name="wm_cap_get_audioformat-message"></a>WM- \_ Cap \_ get \_ Audioformat-Nachricht

Die " **WM \_ Cap \_ get \_ Audioformat** "-Nachricht erhält das Audioformat oder die Größe des Audioformats. Sie können diese Nachricht explizit oder mithilfe der Makros [**capgetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capgetaudioformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) senden.


```C++
WM_CAP_GET_AUDIOFORMAT 
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

Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur oder **null**. Wenn der Wert **null** ist, wird die Größe (in Bytes) zurückgegeben, die zum Speichern der Struktur erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe des Audioformats in Bytes zurück.

## <a name="remarks"></a>Bemerkungen

Da komprimierte Audioformate unterschiedlich groß sind, müssen Anwendungen zuerst die Größe abrufen, dann Arbeitsspeicher zuweisen und schließlich die audioformatdaten anfordern.

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

 

