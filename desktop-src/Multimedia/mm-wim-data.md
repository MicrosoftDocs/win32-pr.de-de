---
title: MM_WIM_DATA Meldung (MMSYSTEM. h)
description: Die mm \_ \_ -WIM-Daten Nachricht wird an ein Fenster gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die waveinreset-Funktion aufgerufen wurde.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA-Nachricht (Multimedia)
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
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338793"
---
# <a name="mm_wim_data-message"></a>MM- \_ WIM- \_ Daten Nachricht

Die **mm- \_ WIM- \_ Daten** Nachricht wird an ein Fenster gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) -Funktion aufgerufen wurde.


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hinputdev*
</dt> <dd>

Handle für das Waveform-Audioeingabegerät, das die Daten empfangen hat.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert, der die Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Puffer ist möglicherweise nicht voll. Verwenden Sie den **dwbyteslock** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die von *LPARAM* angegeben wird, um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden.

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

 

