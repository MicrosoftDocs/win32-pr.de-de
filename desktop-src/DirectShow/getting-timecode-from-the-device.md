---
description: Erhalten von Timecode vom Gerät
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Erhalten von Timecode vom Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344562"
---
# <a name="getting-timecode-from-the-device"></a>Erhalten von Timecode vom Gerät

Wenn ein DV-Band wiedergegeben wird oder sich im Modus zum Anhalten des Datensatzes befindet, können Sie den SMPTE-Zeit Code oder die absolute Nachverfolgung abrufen. Um dies zu erreichen, müssen Sie die [**IAMTimecodeReader:: gettimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) -Methode aufrufen. Diese Methode nimmt einen Zeiger auf eine [**Timecode- \_ Beispiel**](/windows/win32/api/strmif/ns-strmif-timecode_sample) Struktur, die den Zeit Code beschreibt. Initialisieren Sie vor dem Aufrufen der-Methode den **dwFlags** -Member der-Struktur. Verwenden Sie den Wert Ed \_ Devcap \_ Zeitcode \_ Read, um den Zeitcode abzurufen, oder den Wert Ed \_ Devcap \_ Atn \_ Read, um die absolute Nachverfolgung abzurufen.

Der **Zeitcode** -Member der **Zeitcode- \_ Beispiel** Struktur ist eine Zeit Code Struktur. Wenn die-Methode zurückgibt, enthält der **dwframes** -Member der Zeitcode-Struktur den Zeit Code oder die Nachverfolgung. Für Timecode werden die Stunden, Minuten, Sekunden und Frames in einem DWORD-Format als binäre codierte Dezimalwerte (BCD) mit dem Format *hhmmssff* verpackt. Verwenden Sie Bitmasken, um die einzelnen Werte zu extrahieren.

Im folgenden Beispiel werden der Zeitcode und die Nachverfolgung abgerufen.


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

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
