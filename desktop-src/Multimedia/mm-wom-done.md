---
title: MM_WOM_DONE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WOM \_ done wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der wavesetzset-Funktion.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743913"
---
# <a name="mm_wom_done-message"></a>MM- \_ WOM- \_ Nachricht abgeschlossen

Die Meldung **mm \_ WOM \_ done** wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der [**wavesetzset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion.


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*houtputdev*
</dt> <dd>

Handle für das Waveform-Audioausgabegerät, das den Puffer wiedergegeben hat.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

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

 

