---
description: In diesem Thema wird beschrieben, wann und wie eine H. 264/AVC REMUX-MFT-und MP4-Senke verwendet wird.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Verwendung von H. 264/AVC REMUX MFT und MP4-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368261"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="78ad6-103">Verwendung von H. 264/AVC REMUX MFT und MP4-Senke</span><span class="sxs-lookup"><span data-stu-id="78ad6-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="78ad6-104">In diesem Thema wird beschrieben, wann und wie eine H. 264/AVC REMUX-MFT-und MP4-Senke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78ad6-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="78ad6-105">Verwendung von H. 264/AVC REMUX MFT</span><span class="sxs-lookup"><span data-stu-id="78ad6-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="78ad6-106">Das MPEG-4-Dateiformat erfordert, dass jede komprimierte Stichprobe ein primäres Bild mit nal-Einheiten in der richtigen Reihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="78ad6-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="78ad6-107">(Informationen hierzu finden Sie in der Definition der Reihenfolge der primär Bild-und obligatorischen nal-Einheiten im Abschnitt 7.4.1.2.3, in der **Reihenfolge der NAL-Einheiten und in den codierten Bildern und der Zuordnung zu Zugriffs Einheiten** der H. 264 AVC-Spezifikation.) Außerdem ist es erforderlich, dass jedes komprimierte Beispiel einem Präsentationszeit Stempel, dem Decodieren des Zeitstempels und der Stichproben Dauer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78ad6-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="78ad6-108">In vielen Szenarios, in denen Anwendungen H. 264/AVC-Videos in einem MPEG-4-Datei Container aufzeichnen müssen, erfüllt die komprimierte Stichprobe möglicherweise nicht die oben genannten Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="78ad6-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="78ad6-109">Beispielsweise kann eine komprimierte Stichprobe keinen kompletten primär Bild enthalten, oder es ist kein richtiger Präsentationszeit Stempel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="78ad6-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="78ad6-110">Einige Anwendungsbeispiele sind:</span><span class="sxs-lookup"><span data-stu-id="78ad6-110">A few application examples are:</span></span>

-   <span data-ttu-id="78ad6-111">Schreiben Sie das "H. 264/AVC Streaming Elementary Video" in den MPEG-4-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="78ad6-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="78ad6-112">Zeichnen Sie die Kamera mit dem H. 264/AVC-elementaren Video im MPEG-4-Datei Container auf.</span><span class="sxs-lookup"><span data-stu-id="78ad6-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="78ad6-113">Aufzeichnen der H. 264/AVC-Videokonferenz im MPEG-4-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="78ad6-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="78ad6-114">Verketten von zwei H. 264/AVC-Videos in MPEG-2 TS oder MP4 und Schreiben in den MPEG-4-Datei Container mit korrekten Zeitstempeln.</span><span class="sxs-lookup"><span data-stu-id="78ad6-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="78ad6-115">REMUX H. 264/AVC-Video vom AVCHD-, MPEG-2 TS/PS-Dateiformat in das MPEG-4-Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="78ad6-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="78ad6-116">Kürzen der H. 264/AVC-Videodatei ohne Transcoding.</span><span class="sxs-lookup"><span data-stu-id="78ad6-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="78ad6-117">In diesem Fall muss die Anwendung eine H. 264/AVC REMUX-MFT verwenden, um die komprimierten Samples zu konvertieren, die kein vollständiges primär Bild enthalten, bevor Sie in den MPEG-4-Datei Container geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="78ad6-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="78ad6-118">Verwenden von H. 264/AVC REMUX MFT und MP4-Senke</span><span class="sxs-lookup"><span data-stu-id="78ad6-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="78ad6-119">Legen Sie den Medientyp für die Quell Ausgabe auf **mfvideoformat \_ H264 \_ es** fest. Dies bedeutet, dass jedes Beispiel kein vollständiges primär Bild enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="78ad6-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="78ad6-120">Legen Sie den Eingabe Medientyp der MP4-Senke auf **mfvideoformat \_ H264** fest.</span><span class="sxs-lookup"><span data-stu-id="78ad6-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="78ad6-121">Daher ist der Eingabe Medientyp von h. 264/AVC REMUX MFT **mfvideoformat \_ H264 \_ es** , und der Ausgabe Medientyp von h. 264/AVC REMUX MFT ist **mfvideoformat \_ H264**, der automatisch in den topologieresolver eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="78ad6-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="78ad6-122">Die Stichproben Dauer wird von H. 264/AVC REMUX ignoriert, da die Stichproben Dauer für ein Beispiel, das keinen kompletten primär Bild enthält, keine klare Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="78ad6-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="78ad6-123">Stattdessen wird die Stichproben Dauer aus der Framerate berechnet.</span><span class="sxs-lookup"><span data-stu-id="78ad6-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="78ad6-124">Die Framerate wird aus dem Sequenz Parameter berechnet.</span><span class="sxs-lookup"><span data-stu-id="78ad6-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="78ad6-125">Wenn die Informationen nicht im Sequence-Parameter vorhanden sind, wird die Framerate aus den Parametern im Eingabe Medientyp berechnet.</span><span class="sxs-lookup"><span data-stu-id="78ad6-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="78ad6-126">Wenn keine Frameraten Informationen verfügbar sind, wird die Standardbildrate von 29,97 fps verwendet.</span><span class="sxs-lookup"><span data-stu-id="78ad6-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="78ad6-127">H. 264/AVC REMUX MFT linear interpoliert die Decodierungs Zeitstempel (DTS) für jedes komprimierte Bild entsprechend der Framerate.</span><span class="sxs-lookup"><span data-stu-id="78ad6-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="78ad6-128">H. 264/AVC REMUX MFT berücksichtigt die Eingabe Präsentationszeit Stempel (PTS) in Eingabe Beispielen und übergibt sie an die Ausgabe, sofern Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="78ad6-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="78ad6-129">Sie führt die PTS-Interpolation gemäß der Framerate, den vorherigen PTS und der Bild Ausgabe Reihenfolge durch den decodierten Bild Puffer Prozess (DBP) durch, wie in **Anhang C. 4.5.3-bumpingprozess** der H. 264 AVC-Spezifikation angegeben.</span><span class="sxs-lookup"><span data-stu-id="78ad6-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="78ad6-130">Jede Ausgabe Stichprobe aus dem H. 264/AVC REMUX-MFT muss über PTS, DTS und eine Stichproben Dauer verfügen.</span><span class="sxs-lookup"><span data-stu-id="78ad6-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="78ad6-131">H. 264/AVC REMUX MFT identifiziert auch die IDR-Bilder im Bitstrom und legt sie als Clean Point mit dem MF-Attribut des [mfsampleextension- \_ cleanpoints](mfsampleextension-cleanpoint-attribute.md)fest.</span><span class="sxs-lookup"><span data-stu-id="78ad6-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="78ad6-132">Derzeit kann die "H. 264/AVC REMUX"-MFT maximal 64 reorderframe verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="78ad6-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="78ad6-133">Wenn die Anzahl der neu bestellten Frames den Wert 64 mit einem langfristigen Verweis Rahmen überschreitet, Interpolieren die H. 264/AVC REMUX-MFT einen falschen Punkt für diesen Frame und gibt diesen Frame zu einem falschen Zeitpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="78ad6-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="78ad6-134">Um eine h. 264/AVC REMUX-MFT zu instanziieren, legen Sie die richtigen Eingabe-und Ausgabemedien Typen in der H. 264/AVC REMUX-MFT fest, legen Sie den Eingabe Medientyp für die MP4-Senke fest, und beheben Sie die Topologie.</span><span class="sxs-lookup"><span data-stu-id="78ad6-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="78ad6-135">Der folgende Beispielcode zeigt, wie die H. 264/AVC REMUX-MFT und die MP4-Senke initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="78ad6-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="78ad6-136">Für H. 264/AVC REMUX MFT,</span><span class="sxs-lookup"><span data-stu-id="78ad6-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="78ad6-137">Es ist keine weitere Konfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78ad6-137">No further configuration is necessary.</span></span>

<span data-ttu-id="78ad6-138">Für MP4-Senke:</span><span class="sxs-lookup"><span data-stu-id="78ad6-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="78ad6-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78ad6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ad6-140">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78ad6-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



