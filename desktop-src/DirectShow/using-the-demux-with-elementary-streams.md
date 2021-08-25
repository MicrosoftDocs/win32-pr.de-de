---
description: Verwenden von Demux mit elementaren Streams
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Verwenden von Demux mit elementaren Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec805b4c93432c6532edaefac50e9bd15ad8fac5a7d9672fd358c66e57363fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964670"
---
# <a name="using-the-demux-with-elementary-streams"></a>Verwenden von Demux mit elementaren Streams

Wenn die MPEG-2-Demux PES-Nutzlasten übermittelt, sendet sie den ES-Bytestream in Batches von Medienbeispielen. Die Standardbeispielgröße beträgt 8.000. Der Demux startet an jeder PES-Grenze ein neues Medienbeispiel, unterbricht jedoch möglicherweise eine einzelne PES-Nutzlast in mehrere Stichproben. Wenn eine PES-Nutzlast beispielsweise 20.000 beträgt, wird sie in zwei 8K-Beispielen gefolgt von einem 4K-Beispiel übermittelt. Der Demux untersucht nicht den Inhalt des Bytestreams. Der Decoder muss die Sequenzheader analysieren und nach Formatänderungen suchen.

Wenn der Ausgabepin des Demuxfilters eine Verbindung mit dem Decoder herstellt, bietet er den Medientyp, der beim Erstellen des Pins angegeben wurde. Da der Demux den ES-Bytestream nicht untersucht, wird der Medientyp nicht überprüft. Theoretisch sollte ein MPEG-2-Decoder nur mit dem ausgefüllten Haupttyp und Untertyp eine Verbindung herstellen können, um den Datentyp anzugeben. Der Decoder sollte dann die Sequenzheader untersuchen, die in den Medienbeispielen eintreffen. In der Praxis werden viele Decoder jedoch nur dann eine Verbindung herstellen, wenn der Medientyp einen vollständigen Formatblock enthält.

Angenommen, die PID-0x31 MPEG-2-Hauptprofilvideo enthält. Sie müssen mindestens die folgenden Schritte ausführen.

Erstellen Sie zunächst einen Medientyp für MPEG-2-Videos. Lassen Sie den Formatblock vorer mal weg:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Erstellen Sie als Nächstes einen Ausgabepin auf der Demux-Beschriftung:


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



Fragen Sie dann den neuen Pin für die **IMPEG2PIDMap-Schnittstelle** ab, und rufen **Sie MapPID auf.** Geben Sie pid number 0x30 und MEDIA \_ ELEMENTARY \_ STREAM für PES-Nutzlasten an.


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



Lassen Sie abschließend alle Schnittstellen frei, wenn Sie fertig sind:


```C++
pPin0->Release();
pDemux->Release();
```



Hier ist ein vollständigeres Beispiel für das Festlegen des Medientyps, einschließlich des Formatblocks. In diesem Beispiel wird weiterhin ein MPEG-2-Hauptprofilvideo angenommen. Die Details variieren je nach Streaminhalt:


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

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



