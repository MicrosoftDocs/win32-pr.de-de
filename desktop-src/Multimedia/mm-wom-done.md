---
title: MM_WOM_DONE Meldung (Mmsystem.h)
description: Die \_ MM WOM \_ DONE-Nachricht wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn sie wiedergegeben wurden, oder als Ergebnis eines Aufrufs der waveOutReset-Funktion.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE nachricht Windows Multimedia
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
ms.openlocfilehash: 225ba32f780831ab8b40f487a312a940219abc2e976be75a4e903648344afc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065460"
---
# <a name="mm_wom_done-message"></a>MM \_ WOM \_ DONE-Meldung

Die **MM \_ WOM \_ DONE-Nachricht** wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn sie wiedergegeben wurden, oder als Ergebnis eines Aufrufs der [**waveOutReset-Funktion.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle für das Waveform-Audio-Ausgabegerät, das den Puffer wiedergegeben hat.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Zeiger auf eine [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) die den Puffer identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

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

 

