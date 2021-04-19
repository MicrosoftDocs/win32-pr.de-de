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
# <a name="using-the-demux-with-psi-streams"></a>Verwenden von "de MUX" mit PSI-Streams

Um psi-Informationen aus einem MPEG-2-Transportdaten Strom mithilfe des MPEG-2-Demux-Filters zu erhalten, erstellen Sie eine Ausgabe-PIN für die Demux-Datei mit dem folgenden Medientyp:

-   Haupttyp: "ksdataformat"- \_ Typ " \_ MPEG2" \_
-   Untertyp: mediasubtype \_ None
-   Formattyp: GUID \_ null

Dann wenden Sie die [**IMPEG2PIDMap:: mappid**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) -Methode der Ausgabe-PIN mit der gewünschten PID und dem Flag Media \_ MPEG2 \_ PSI an.


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



Jeder gesamte PSI-Abschnitt wird in einem Beispiel für ein Medium bereitgestellt. Rufen Sie zum Abrufen der mit einem Tabellen Abschnitt verknüpften PID-Nummer [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Medien Beispiel auf. Die PID ist in den unteren 13 Bits des **dwtypespecificflags-Flags** in der **am \_ SAMPLE2 \_ Properties** -Struktur angegeben. Dies ist hilfreich, wenn Sie dem gleichen Ausgabepin mehrere PSI-PIDs zuordnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



