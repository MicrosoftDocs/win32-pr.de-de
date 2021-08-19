---
title: Bestimmen der Nichtstandardformatunterstützung
description: Bestimmen der Nichtstandardformatunterstützung
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- Waveformaudio, Nichtstandardformatunterstützung
- Zusätzliche Audioinhalte, Unterstützung von formatfremden Formaten
- Waveformaudio, Unterstützung des Standardformats
- Zusatzaudio, Unterstützung des Standardformats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a90d38f7419b6fbdb3de951c0aa2205ccd3dd9ff5366eb1e69eab945220db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497280"
---
# <a name="determining-nonstandard-format-support"></a>Bestimmen der Nichtstandardformatunterstützung

Um festzustellen, ob ein Gerät ein bestimmtes Format unterstützt (Standard oder nicht standard), können Sie die [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) mit dem WAVE \_ FORMAT \_ QUERY-Flag aufrufen. Im folgenden Beispiel wird dieses Verfahren verwendet, um zu bestimmen, ob ein Waveform-Audiogerät ein angegebenes Format unterstützt.


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



Dieses Verfahren zum Bestimmen der Nichtstandardformatunterstützung gilt auch für Waveform-Audio-Eingabegeräte. Der einzige Unterschied besteht darin, dass die [**waveInOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) anstelle von [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) verwendet wird, um Formatunterstützung abzufragen.

Um zu bestimmen, ob ein bestimmtes Waveform-Audio-Datenformat von einem der Waveform-Audio-Geräte in einem System unterstützt wird, verwenden Sie die im vorherigen Beispiel gezeigte Technik, geben aber die WAVE \_ MAPPER-Konstante für den *uDeviceID-Parameter* an.

 

 