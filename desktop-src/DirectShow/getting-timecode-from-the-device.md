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
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="33112-103">Erhalten von Timecode vom Gerät</span><span class="sxs-lookup"><span data-stu-id="33112-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="33112-104">Wenn ein DV-Band wiedergegeben wird oder sich im Modus zum Anhalten des Datensatzes befindet, können Sie den SMPTE-Zeit Code oder die absolute Nachverfolgung abrufen.</span><span class="sxs-lookup"><span data-stu-id="33112-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="33112-105">Um dies zu erreichen, müssen Sie die [**IAMTimecodeReader:: gettimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="33112-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="33112-106">Diese Methode nimmt einen Zeiger auf eine [**Timecode- \_ Beispiel**](/windows/win32/api/strmif/ns-strmif-timecode_sample) Struktur, die den Zeit Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="33112-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="33112-107">Initialisieren Sie vor dem Aufrufen der-Methode den **dwFlags** -Member der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="33112-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="33112-108">Verwenden Sie den Wert Ed \_ Devcap \_ Zeitcode \_ Read, um den Zeitcode abzurufen, oder den Wert Ed \_ Devcap \_ Atn \_ Read, um die absolute Nachverfolgung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="33112-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="33112-109">Der **Zeitcode** -Member der **Zeitcode- \_ Beispiel** Struktur ist eine Zeit Code Struktur.</span><span class="sxs-lookup"><span data-stu-id="33112-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="33112-110">Wenn die-Methode zurückgibt, enthält der **dwframes** -Member der Zeitcode-Struktur den Zeit Code oder die Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="33112-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="33112-111">Für Timecode werden die Stunden, Minuten, Sekunden und Frames in einem DWORD-Format als binäre codierte Dezimalwerte (BCD) mit dem Format *hhmmssff* verpackt.</span><span class="sxs-lookup"><span data-stu-id="33112-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="33112-112">Verwenden Sie Bitmasken, um die einzelnen Werte zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="33112-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="33112-113">Im folgenden Beispiel werden der Zeitcode und die Nachverfolgung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="33112-113">The following example retrieves the timecode and track number.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="33112-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33112-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33112-115">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="33112-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
