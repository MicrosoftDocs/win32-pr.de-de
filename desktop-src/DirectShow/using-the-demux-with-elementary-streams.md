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
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="1d729-103">Verwenden von "REMUX" mit elementaren Datenströmen</span><span class="sxs-lookup"><span data-stu-id="1d729-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="1d729-104">Wenn MPEG-2 Demux PE-Nutzlasten bereitstellt, sendet es den es-Bytestream in Batches von Medien Beispielen.</span><span class="sxs-lookup"><span data-stu-id="1d729-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="1d729-105">Die standardmäßige Stichprobengröße beträgt 8K.</span><span class="sxs-lookup"><span data-stu-id="1d729-105">The default sample size is 8K.</span></span> <span data-ttu-id="1d729-106">Die "Debug" startet ein neues Medien Beispiel für jede PES-Grenze, kann jedoch eine einzelne PES-Nutzlast in mehrere Beispiele unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="1d729-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="1d729-107">Wenn eine PES-Nutzlast z. b. 20K beträgt, wird Sie in zwei 8-KB-Stichproben gefolgt von einem 4K-Beispiel geliefert.</span><span class="sxs-lookup"><span data-stu-id="1d729-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="1d729-108">Der Inhalt des Bytestreams wird von der Demux nicht untersucht.</span><span class="sxs-lookup"><span data-stu-id="1d729-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="1d729-109">Der Decoder muss die Sequenz Header analysieren und nach Formatänderungen suchen.</span><span class="sxs-lookup"><span data-stu-id="1d729-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="1d729-110">Wenn die Ausgabe-PIN des Demux-Filters eine Verbindung mit dem Decoder herstellt, bietet Sie den Medientyp an, der beim Erstellen der PIN angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1d729-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="1d729-111">Da die Demux den es-Byte Datenstrom nicht untersucht, wird der Medientyp nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="1d729-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="1d729-112">Theoretisch sollte ein MPEG-2-Decoder nur mit dem größten Typ und Untertyp, der ausgefüllt ist, eine Verbindung herstellen können, um den Datentyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d729-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="1d729-113">Der Decoder sollte dann die Sequenz Header untersuchen, die in den Medien Beispielen eintreffen.</span><span class="sxs-lookup"><span data-stu-id="1d729-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="1d729-114">In der Praxis werden jedoch viele Decoder nur dann verbunden, wenn der Medientyp einen kompletten Format Block enthält.</span><span class="sxs-lookup"><span data-stu-id="1d729-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="1d729-115">Nehmen Sie beispielsweise an, dass die PID 0x31 das MPEG-2-Hauptprofil Video enthält.</span><span class="sxs-lookup"><span data-stu-id="1d729-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="1d729-116">Sie müssen mindestens die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d729-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="1d729-117">Erstellen Sie zunächst einen Medientyp für das MPEG-2-Video.</span><span class="sxs-lookup"><span data-stu-id="1d729-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="1d729-118">Der Format Block wird vorerst nicht mehr angezeigt:</span><span class="sxs-lookup"><span data-stu-id="1d729-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="1d729-119">Erstellen Sie als nächstes eine Ausgabe-PIN auf der Demux-Datei:</span><span class="sxs-lookup"><span data-stu-id="1d729-119">Next, create an output pin on the demux:</span></span>


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



<span data-ttu-id="1d729-120">Fragen Sie dann die neue PIN der **IMPEG2PIDMap** -Schnittstelle ab, und nennen Sie **mappid**.</span><span class="sxs-lookup"><span data-stu-id="1d729-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="1d729-121">Geben Sie die PID-Nummer 0x30 und den Medien \_ elementaren \_ Stream für PE-Nutzlasten an.</span><span class="sxs-lookup"><span data-stu-id="1d729-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


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



<span data-ttu-id="1d729-122">Geben Sie abschließend alle Schnittstellen frei, wenn Sie dies abgeschlossen haben:</span><span class="sxs-lookup"><span data-stu-id="1d729-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="1d729-123">Im folgenden finden Sie ein ausführeres Beispiel für das Festlegen des Medientyps, einschließlich des Format Blocks.</span><span class="sxs-lookup"><span data-stu-id="1d729-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="1d729-124">In diesem Beispiel wird weiterhin ein MPEG-2-Hauptprofil-Video angenommen.</span><span class="sxs-lookup"><span data-stu-id="1d729-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="1d729-125">Die Details variieren abhängig von den Datenstrom Inhalten:</span><span class="sxs-lookup"><span data-stu-id="1d729-125">The details will vary depending on stream contents:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1d729-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d729-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d729-127">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="1d729-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



