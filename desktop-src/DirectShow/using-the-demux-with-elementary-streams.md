---
description: Verwenden von "REMUX" mit elementaren Datenströmen
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Verwenden von "REMUX" mit elementaren Datenströmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346398"
---
# <a name="using-the-demux-with-elementary-streams"></a>Verwenden von "REMUX" mit elementaren Datenströmen

Wenn MPEG-2 Demux PE-Nutzlasten bereitstellt, sendet es den es-Bytestream in Batches von Medien Beispielen. Die standardmäßige Stichprobengröße beträgt 8K. Die "Debug" startet ein neues Medien Beispiel für jede PES-Grenze, kann jedoch eine einzelne PES-Nutzlast in mehrere Beispiele unterbrechen. Wenn eine PES-Nutzlast z. b. 20K beträgt, wird Sie in zwei 8-KB-Stichproben gefolgt von einem 4K-Beispiel geliefert. Der Inhalt des Bytestreams wird von der Demux nicht untersucht. Der Decoder muss die Sequenz Header analysieren und nach Formatänderungen suchen.

Wenn die Ausgabe-PIN des Demux-Filters eine Verbindung mit dem Decoder herstellt, bietet Sie den Medientyp an, der beim Erstellen der PIN angegeben wurde. Da die Demux den es-Byte Datenstrom nicht untersucht, wird der Medientyp nicht überprüft. Theoretisch sollte ein MPEG-2-Decoder nur mit dem größten Typ und Untertyp, der ausgefüllt ist, eine Verbindung herstellen können, um den Datentyp anzugeben. Der Decoder sollte dann die Sequenz Header untersuchen, die in den Medien Beispielen eintreffen. In der Praxis werden jedoch viele Decoder nur dann verbunden, wenn der Medientyp einen kompletten Format Block enthält.

Nehmen Sie beispielsweise an, dass die PID 0x31 das MPEG-2-Hauptprofil Video enthält. Sie müssen mindestens die folgenden Schritte ausführen.

Erstellen Sie zunächst einen Medientyp für das MPEG-2-Video. Der Format Block wird vorerst nicht mehr angezeigt:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Erstellen Sie als nächstes eine Ausgabe-PIN auf der Demux-Datei:


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



Fragen Sie dann die neue PIN der **IMPEG2PIDMap** -Schnittstelle ab, und nennen Sie **mappid**. Geben Sie die PID-Nummer 0x30 und den Medien \_ elementaren \_ Stream für PE-Nutzlasten an.


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



Geben Sie abschließend alle Schnittstellen frei, wenn Sie dies abgeschlossen haben:


```C++
pPin0->Release();
pDemux->Release();
```



Im folgenden finden Sie ein ausführeres Beispiel für das Festlegen des Medientyps, einschließlich des Format Blocks. In diesem Beispiel wird weiterhin ein MPEG-2-Hauptprofil-Video angenommen. Die Details variieren abhängig von den Datenstrom Inhalten:


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



