---
title: WOM_DONE (Mmsystem.h)
description: Die WOM DONE-Nachricht wird an eine Waveform-Audio-Ausgaberückruffunktion gesendet, wenn der gegebene Ausgabepuffer \_ an die Anwendung zurückgegeben wird.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8e54fe6f8f79c9fe5885861dbda758a663ca49b38ed559b06ba59627768055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134815"
---
# <a name="wom_done-message"></a>WOM \_ DONE-Nachricht

Die **WOM \_ DONE-Nachricht** wird an eine Waveform-Audio-Ausgaberückruffunktion gesendet, wenn der gegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn sie abgespielt wurden, oder als Ergebnis eines Aufrufs der [**waveOutReset-Funktion.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Zeiger auf eine [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die den Puffer identifiziert.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Waveform-Nachrichten](waveform-messages.md)
</dt> </dl>

 

