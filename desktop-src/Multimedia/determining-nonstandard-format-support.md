---
title: Festlegen der nicht standardmäßigen Format Unterstützung
description: Festlegen der nicht standardmäßigen Format Unterstützung
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- Wellenform-Audiounterstützung, nicht dem Standard entsprechende Formatunterstützung
- zusätzliche Audiounterstützung, nicht dem Standard entsprechende Formatunterstützung
- Wellenform-Audiounterstützung, Standardformat Unterstützung
- hilfsaudiounterstützung, Standardformat Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038902"
---
# <a name="determining-nonstandard-format-support"></a>Festlegen der nicht standardmäßigen Format Unterstützung

Wenn Sie feststellen möchten, ob ein Gerät ein bestimmtes Format (Standard oder nicht Standard) unterstützt, können Sie die [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion mit dem Query-Flag "Wave Format" aufzurufen \_ \_ . Das folgende Beispiel verwendet dieses Verfahren, um zu bestimmen, ob ein Waveform-Audiogerät ein bestimmtes Format unterstützt.


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



Dieses Verfahren zum Bestimmen der nicht standardmäßigen Formatunterstützung gilt auch für Waveform-Audioeingabegeräte. Der einzige Unterschied besteht darin, dass die [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion anstelle von [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) verwendet wird, um die Formatunterstützung abzufragen.

Um zu ermitteln, ob ein bestimmtes Waveform-Audiodatenformat von einem der Waveform-Audiogeräte in einem System unterstützt wird, verwenden Sie die im vorherigen Beispiel veranschaulichte Technik, aber geben Sie die Wave- \_ Mapper-Konstante für den *udeviceid* -Parameter an.

 

 