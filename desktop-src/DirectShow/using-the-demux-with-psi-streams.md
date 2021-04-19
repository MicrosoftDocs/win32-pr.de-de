---
description: Verwenden von "de MUX" mit PSI-Streams
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Verwenden von "de MUX" mit PSI-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373142"
---
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="c9ef9-103">Verwenden von "de MUX" mit PSI-Streams</span><span class="sxs-lookup"><span data-stu-id="c9ef9-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="c9ef9-104">Um psi-Informationen aus einem MPEG-2-Transportdaten Strom mithilfe des MPEG-2-Demux-Filters zu erhalten, erstellen Sie eine Ausgabe-PIN für die Demux-Datei mit dem folgenden Medientyp:</span><span class="sxs-lookup"><span data-stu-id="c9ef9-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="c9ef9-105">Haupttyp: "ksdataformat"- \_ Typ " \_ MPEG2" \_</span><span class="sxs-lookup"><span data-stu-id="c9ef9-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="c9ef9-106">Untertyp: mediasubtype \_ None</span><span class="sxs-lookup"><span data-stu-id="c9ef9-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="c9ef9-107">Formattyp: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="c9ef9-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="c9ef9-108">Dann wenden Sie die [**IMPEG2PIDMap:: mappid**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) -Methode der Ausgabe-PIN mit der gewünschten PID und dem Flag Media \_ MPEG2 \_ PSI an.</span><span class="sxs-lookup"><span data-stu-id="c9ef9-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



<span data-ttu-id="c9ef9-109">Jeder gesamte PSI-Abschnitt wird in einem Beispiel für ein Medium bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9ef9-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="c9ef9-110">Rufen Sie zum Abrufen der mit einem Tabellen Abschnitt verknüpften PID-Nummer [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Medien Beispiel auf.</span><span class="sxs-lookup"><span data-stu-id="c9ef9-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="c9ef9-111">Die PID ist in den unteren 13 Bits des **dwtypespecificflags-Flags** in der **am \_ SAMPLE2 \_ Properties** -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9ef9-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="c9ef9-112">Dies ist hilfreich, wenn Sie dem gleichen Ausgabepin mehrere PSI-PIDs zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c9ef9-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9ef9-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9ef9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9ef9-114">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="c9ef9-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



