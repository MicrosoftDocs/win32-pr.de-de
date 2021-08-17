---
title: MM_WIM_DATA Meldung (Mmsystem.h)
description: Die MM \_ WIM \_ DATA-Nachricht wird an ein Fenster gesendet, wenn waveform-audio-Daten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die waveInReset-Funktion aufgerufen wurde.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b209e59032c0da4c875a316008c889cf064ae7d8bc48f5c621125a06582673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065470"
---
# <a name="mm_wim_data-message"></a>MM \_ WIM \_ DATA-Nachricht

Die **MM \_ WIM \_ DATA-Nachricht** wird an ein Fenster gesendet, wenn waveform-audio-Daten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveInReset-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) aufgerufen wurde.


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle für das Waveform-Audio-Eingabegerät, das die Daten empfangen hat.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Zeiger auf eine [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die den Puffer identifiziert, der die Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Puffer ist möglicherweise nicht voll. Verwenden Sie den **dwBytesRecorded-Member** der [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die von *lParam* angegeben wird, um die Anzahl der bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Wellenformnachrichten](waveform-messages.md)
</dt> </dl>

 

