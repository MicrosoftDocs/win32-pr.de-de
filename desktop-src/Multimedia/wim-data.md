---
title: WIM_DATA (Mmsystem.h)
description: Die WIM DATA-Nachricht wird an die angegebenen Waveform-Audio-Eingaberückruffunktion gesendet, wenn waveform-audio-Daten im Eingabepuffer vorhanden sind und der Puffer an die \_ Anwendung zurückgegeben wird.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956dacefa507c2c92f05afdd39bc9c803c630421c81620e0320f3b06648b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940748"
---
# <a name="wim_data-message"></a>WIM \_ DATA-Nachricht

Die **WIM \_ DATA-Nachricht** wird an die angegebenen Waveform-Audio-Eingaberückruffunktion gesendet, wenn waveform-audio-Daten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveInReset-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) aufgerufen wurde.


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Zeiger auf eine [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die den Puffer identifiziert, der die Daten enthält.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Puffer ist möglicherweise nicht voll. Verwenden Sie **den dwBytesRecorded-Member** der [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die von *lpwvhdr* angegeben wird, um die Anzahl der in den zurückgegebenen Puffer aufgezeichneten Bytes zu bestimmen.

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

[Waveform-Nachrichten](waveform-messages.md)
</dt> </dl>

 

