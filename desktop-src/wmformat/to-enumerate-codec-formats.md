---
title: So aufzählen Sie Codecformate
description: So aufzählen Sie Codecformate
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- Streams,Aufzählen von Codecformaten
- Codecs,Enumerationen
- Streams, Codecformate
- Codecs,Formate
- codecs,IWMCodecInfo-Schnittstelle
- IWMCodecInfo,Codec-Formate
- codecs,IWMCodecInfo3-Schnittstelle
- IWMCodecInfo3, Codecformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444781"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="c4185-111">So aufzählen Sie Codecformate</span><span class="sxs-lookup"><span data-stu-id="c4185-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="c4185-112">Ein Codecformat ist ein Streamkonfigurationsobjekt, das mit Daten aus einem Codec aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c4185-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="c4185-113">Jedes Codecformat enthält eine vom Codec unterstützte Medienkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4185-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="c4185-114">Die meisten Audiocodecs unterstützen eine begrenzte Anzahl von Formaten, von denen jedes vom Codec aufzählt wird und auf die mithilfe der [**Methoden von IWMCodecInfo zugegriffen werden kann.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)</span><span class="sxs-lookup"><span data-stu-id="c4185-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="c4185-115">Videocodecs bieten dagegen nur ein einzelnes Format.</span><span class="sxs-lookup"><span data-stu-id="c4185-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="c4185-116">Dies liegt daran, dass Videostreams Variablen wie die Framegröße haben, die flexibler als die Einstellungen eines Audiostreams sind.</span><span class="sxs-lookup"><span data-stu-id="c4185-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="c4185-117">Mit einem Videostream müssen Sie einige der Streamkonfigurationswerte ausfüllen. Audiostreamkonfigurationen sollten nur bearbeitet werden, um einen Namen, einen Verbindungsnamen und eine Streamnummer zu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c4185-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="c4185-118">Weitere Informationen finden Sie unter [Allgemeine Konfiguration für alle Streams.](configuration-common-to-all-streams.md)</span><span class="sxs-lookup"><span data-stu-id="c4185-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="c4185-119">Die aufgelisteten Codecformate hängen von den aktuellen Codecenumerationseinstellungen ab, die [**mitHILFE von IWMCodecInfo3::SetCodecEnumerationSetting festgelegt werden.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting)</span><span class="sxs-lookup"><span data-stu-id="c4185-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="c4185-120">Derzeit werden nur zwei Codeceigenschaften unterstützt: g wszNumPasses, das die Anzahl der vom Codec durchzuführenden Codierungsüberläufe angibt, und \_ g wszVBREnabled, das angibt, ob der Codec die Codierung mit variabler Bitrate \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4185-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="c4185-121">Die maximale Anzahl von Codierungsüberläufen, die von einem der Codecs unterstützt werden, beträgt zwei. Daher gibt es vier unterschiedliche Konfigurationen, für die Sie Codecs abrufen können, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4185-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|    &nbsp;    | <span data-ttu-id="c4185-122">CBR-Stream (Constant Bit Rate)</span><span class="sxs-lookup"><span data-stu-id="c4185-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="c4185-123">2-Pass-CBR-Stream</span><span class="sxs-lookup"><span data-stu-id="c4185-123">2-pass CBR stream</span></span> | <span data-ttu-id="c4185-124">Qualitätsbasierter Stream mit variabler Bitrate (VBR)</span><span class="sxs-lookup"><span data-stu-id="c4185-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="c4185-125">Bitratenbasierter VBR-Stream (eingeschränkt oder nicht eingeschränkt)</span><span class="sxs-lookup"><span data-stu-id="c4185-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4185-126">g \_ wszVBREnabled</span><span class="sxs-lookup"><span data-stu-id="c4185-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="c4185-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4185-127">FALSE</span></span>                          | <span data-ttu-id="c4185-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4185-128">FALSE</span></span>             | <span data-ttu-id="c4185-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4185-129">TRUE</span></span>                                         | <span data-ttu-id="c4185-130">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4185-130">TRUE</span></span>                                                     |
| <span data-ttu-id="c4185-131">g \_ wszNumPasses</span><span class="sxs-lookup"><span data-stu-id="c4185-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="c4185-132">1</span><span class="sxs-lookup"><span data-stu-id="c4185-132">1</span></span>                              | <span data-ttu-id="c4185-133">2</span><span class="sxs-lookup"><span data-stu-id="c4185-133">2</span></span>                 | <span data-ttu-id="c4185-134">1</span><span class="sxs-lookup"><span data-stu-id="c4185-134">1</span></span>                                            | <span data-ttu-id="c4185-135">2</span><span class="sxs-lookup"><span data-stu-id="c4185-135">2</span></span>                                                        |



 

<span data-ttu-id="c4185-136">Um die für einen Codec unterstützten Formate zu aufzählen, verwenden Sie [**IWMCodecInfo::GetCodecFormatCount,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) um die Anzahl der unterstützten Codecs zu finden.</span><span class="sxs-lookup"><span data-stu-id="c4185-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="c4185-137">Rufen Sie [**dann IWMCodecInfo::GetCodecFormat für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) jedes Format auf.</span><span class="sxs-lookup"><span data-stu-id="c4185-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="c4185-138">Die Formatindizes reichen von 0 (null) bis zu einem Wert kleiner als die Gesamtzahl der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="c4185-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="c4185-139">Sie können eine Beschreibung des Formats abrufen, indem Sie [**IWMCodecInfo2::GetCodecFormatDesc aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)</span><span class="sxs-lookup"><span data-stu-id="c4185-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="c4185-140">Bei Verwendung **von GetCodecFormatDesc** müssen Sie **GetCodecFormat** nicht verwenden, da das Streamkonfigurationsobjekt von beiden Methoden abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4185-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="c4185-141">Videocodecformate enthalten keine Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="c4185-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="c4185-142">Jeder Videocodec hat nur ein Format, das für alle Streams dieses Typs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4185-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="c4185-143">Wenn Sie ein Codecformat abrufen, erhalten Sie die [**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) eines Streamkonfigurationsobjekts, das die Formateinstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c4185-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4185-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4185-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4185-145">**Abrufen von Streamkonfigurationsinformationen aus Codecs**</span><span class="sxs-lookup"><span data-stu-id="c4185-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




