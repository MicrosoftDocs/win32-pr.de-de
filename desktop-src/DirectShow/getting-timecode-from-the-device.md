---
description: Abrufen von Timecode vom Gerät
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Abrufen von Timecode vom Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265769300c0134ec9f3b3635ada3e595205e8452ced262d4062f9fb6cdaaadc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564730"
---
# <a name="getting-timecode-from-the-device"></a>Abrufen von Timecode vom Gerät

Während ein DV-Band wiedergegeben wird oder sich im Aufzeichnungspausenmodus befindet, können Sie den SMPTE-Zeitcode oder die absolute Tracknummer abrufen. Rufen Sie hierzu die [**IAMTimecodeReader::GetTimecode-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) auf. Diese Methode verwendet einen Zeiger auf eine [**TIMECODE \_ SAMPLE-Struktur,**](/windows/win32/api/strmif/ns-strmif-timecode_sample) die den Zeitcode beschreibt. Initialisieren Sie vor dem Aufrufen der -Methode den **dwFlags-Member** der -Struktur. Verwenden Sie den Wert ED \_ DEVCAP \_ TIMECODE \_ READ, um den Timecode abzurufen, oder den Wert ED \_ DEVCAP \_ ATN \_ READ, um die absolute Tracknummer abzurufen.

Der **Timecodemember** der **TIMECODE \_ SAMPLE-Struktur** ist eine TIMECODE-Struktur. Wenn die Methode zurückgegeben wird, enthält der **dwFrames-Member** der TIMECODE-Struktur den Timecode oder die Tracknummer. Für timecode werden die Stunden, Minuten, Sekunden und Frames als binär codierte Dezimalwerte (Binary Coded Decimal, BCD) mit dem Format *hhmmssff* in ein DWORD gepackt. Verwenden Sie Bitmasken, um die einzelnen Werte zu extrahieren.

Im folgenden Beispiel werden der Zeitcode und die Nachverfolgungsnummer abgerufen.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
