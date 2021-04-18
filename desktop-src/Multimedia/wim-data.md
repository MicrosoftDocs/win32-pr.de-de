---
title: WIM_DATA Meldung (MMSYSTEM. h)
description: Die WIM \_ -Daten Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA-Nachricht (Multimedia)
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
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340365"
---
# <a name="wim_data-message"></a>Wim- \_ Daten Nachricht

Die **WIM- \_ Daten** Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) -Funktion aufgerufen wurde.


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert, der die Daten enthält.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Puffer ist möglicherweise nicht voll. Verwenden Sie den **dwbyteslock** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die von *lpwvhdr* angegeben wird, um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audiodatei](waveform-audio.md)
</dt> <dt>

[Wellenform Meldungen](waveform-messages.md)
</dt> </dl>

 

