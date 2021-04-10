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
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="d392a-107">Festlegen der nicht standardmäßigen Format Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d392a-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="d392a-108">Wenn Sie feststellen möchten, ob ein Gerät ein bestimmtes Format (Standard oder nicht Standard) unterstützt, können Sie die [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion mit dem Query-Flag "Wave Format" aufzurufen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d392a-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="d392a-109">Das folgende Beispiel verwendet dieses Verfahren, um zu bestimmen, ob ein Waveform-Audiogerät ein bestimmtes Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d392a-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


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



<span data-ttu-id="d392a-110">Dieses Verfahren zum Bestimmen der nicht standardmäßigen Formatunterstützung gilt auch für Waveform-Audioeingabegeräte.</span><span class="sxs-lookup"><span data-stu-id="d392a-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="d392a-111">Der einzige Unterschied besteht darin, dass die [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion anstelle von [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) verwendet wird, um die Formatunterstützung abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d392a-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="d392a-112">Um zu ermitteln, ob ein bestimmtes Waveform-Audiodatenformat von einem der Waveform-Audiogeräte in einem System unterstützt wird, verwenden Sie die im vorherigen Beispiel veranschaulichte Technik, aber geben Sie die Wave- \_ Mapper-Konstante für den *udeviceid* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="d392a-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 