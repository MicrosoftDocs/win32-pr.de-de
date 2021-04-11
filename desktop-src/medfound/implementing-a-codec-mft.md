---
description: Dieses Thema enthält einige Richtlinien für die Implementierung eines Decoders oder Encoders als Media Foundation Transformation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementieren eines Codec-MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218244"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="4c317-103">Implementieren eines Codec-MFT</span><span class="sxs-lookup"><span data-stu-id="4c317-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="4c317-104">Dieses Thema enthält einige Richtlinien für die Implementierung eines Decoders oder Encoders als Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="4c317-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="4c317-105">Encoder</span><span class="sxs-lookup"><span data-stu-id="4c317-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="4c317-106">Aushandlung des encoderformats</span><span class="sxs-lookup"><span data-stu-id="4c317-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="4c317-107">Decoder</span><span class="sxs-lookup"><span data-stu-id="4c317-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="4c317-108">Nur-transcode-decoderer</span><span class="sxs-lookup"><span data-stu-id="4c317-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="4c317-109">Telecine-Attribute</span><span class="sxs-lookup"><span data-stu-id="4c317-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="4c317-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c317-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="4c317-111">Encoder</span><span class="sxs-lookup"><span data-stu-id="4c317-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="4c317-112">Aushandlung des encoderformats</span><span class="sxs-lookup"><span data-stu-id="4c317-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="4c317-113">Das folgende Verfahren wird verwendet, um einen Encoder zu initialisieren:</span><span class="sxs-lookup"><span data-stu-id="4c317-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="4c317-114">Fragen Sie die MFT für die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4c317-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="4c317-115">Aufrufen von [**icodecapi:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) , um Codierungs Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4c317-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="4c317-116">Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um das Codierungsformat festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4c317-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="4c317-117">Wenn Sie [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) aufrufen, erhalten Sie eine Liste der kompatiblen Eingabetypen.</span><span class="sxs-lookup"><span data-stu-id="4c317-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="4c317-118">(Dieser Schritt kann übersprungen werden.)</span><span class="sxs-lookup"><span data-stu-id="4c317-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="4c317-119">Um das unkomprimierte Eingabeformat festzulegen, wird [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4c317-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="4c317-120">Nachdem der Ausgabetyp in Schritt 3 festgelegt wurde, muss die [**getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) -Methode eine Liste von Eingabetypen zurückgeben, die mit dem aktuellen Ausgabetyp kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="4c317-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="4c317-121">Dies bedeutet, dass alle von **getinputavailabletype** an dieser Stelle zurückgegebenen Typen für " [**tartinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)" gültig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="4c317-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="4c317-122">Für Decoders wird die Reihenfolge, in der die Typen festgelegt werden, umgekehrt: der Eingabetyp wird zuerst festgelegt, gefolgt vom Ausgabetyp.</span><span class="sxs-lookup"><span data-stu-id="4c317-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="4c317-123">Nachdem der Eingabetyp festgelegt wurde, muss die [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode eine Liste von Typen zurückgeben, die an die [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode weitergegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4c317-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="4c317-124">Encoder und Decoder sollten NV12 als häufiges nicht komprimiertes Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4c317-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="4c317-125">Dadurch wird sichergestellt, dass Pipeline Komponenten mit minimalen colorspace-Konvertierungen interagieren können.</span><span class="sxs-lookup"><span data-stu-id="4c317-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="4c317-126">Natürlich können auch andere Formate unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4c317-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="4c317-127">Decoder</span><span class="sxs-lookup"><span data-stu-id="4c317-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="4c317-128">Transcode-Only Decoders</span><span class="sxs-lookup"><span data-stu-id="4c317-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="4c317-129">Einige Decoder sind für das transcodieren optimiert (decodieren und erneutes Codieren eines Streams) und sind nicht für die Verwendung während der Wiedergabe geeignet.</span><span class="sxs-lookup"><span data-stu-id="4c317-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="4c317-130">Wenn ein Decoder-MFT nur für die Transcodierung vorgesehen ist, legen Sie das Flag für die **MFT- \_ Enum- \_ Flag \_ \_ nur transcode** fest, wenn Sie die MFT registrieren.</span><span class="sxs-lookup"><span data-stu-id="4c317-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="4c317-131">(Weitere Informationen finden Sie unter [**MF tregiester**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span><span class="sxs-lookup"><span data-stu-id="4c317-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="4c317-132">Standardmäßig werden transcodieren-Decoder nicht von der [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4c317-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="4c317-133">Zum Auflisten von transcodieren-Decodern müssen Sie **mftenumex** aufrufen und das Flag für die MFT-Enumeration für **\_ \_ \_ transcodieren \_ only** im *Flags* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="4c317-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="4c317-134">Bei Verwendung in der **msumex** -Funktion zählt dieses Flag sowohl transcodieren-Decoder als auch andere Decoder auf.</span><span class="sxs-lookup"><span data-stu-id="4c317-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="4c317-135">Mftregiester-MFT-Aufzählungs **\_ \_ Flag \_ \_ nur transcode**</span><span class="sxs-lookup"><span data-stu-id="4c317-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="4c317-136">Mftenumex-MFT-Aufzählungs **\_ \_ Flag \_ \_ nur transcode**</span><span class="sxs-lookup"><span data-stu-id="4c317-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="4c317-137">Ist MFT aufgezählt?</span><span class="sxs-lookup"><span data-stu-id="4c317-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="4c317-138">1</span><span class="sxs-lookup"><span data-stu-id="4c317-138">1</span></span>                                                | <span data-ttu-id="4c317-139">1</span><span class="sxs-lookup"><span data-stu-id="4c317-139">1</span></span>                                              | <span data-ttu-id="4c317-140">Ja</span><span class="sxs-lookup"><span data-stu-id="4c317-140">Yes</span></span>                |
| <span data-ttu-id="4c317-141">1</span><span class="sxs-lookup"><span data-stu-id="4c317-141">1</span></span>                                                | <span data-ttu-id="4c317-142">0</span><span class="sxs-lookup"><span data-stu-id="4c317-142">0</span></span>                                              | <span data-ttu-id="4c317-143">Nein</span><span class="sxs-lookup"><span data-stu-id="4c317-143">No</span></span>                 |
| <span data-ttu-id="4c317-144">0</span><span class="sxs-lookup"><span data-stu-id="4c317-144">0</span></span>                                                | <span data-ttu-id="4c317-145">1</span><span class="sxs-lookup"><span data-stu-id="4c317-145">1</span></span>                                              | <span data-ttu-id="4c317-146">Ja</span><span class="sxs-lookup"><span data-stu-id="4c317-146">Yes</span></span>                |
| <span data-ttu-id="4c317-147">0</span><span class="sxs-lookup"><span data-stu-id="4c317-147">0</span></span>                                                | <span data-ttu-id="4c317-148">0</span><span class="sxs-lookup"><span data-stu-id="4c317-148">0</span></span>                                              | <span data-ttu-id="4c317-149">Ja</span><span class="sxs-lookup"><span data-stu-id="4c317-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="4c317-150">Telecine-Attribute</span><span class="sxs-lookup"><span data-stu-id="4c317-150">Telecine Attributes</span></span>

<span data-ttu-id="4c317-151">Die Medienquelle kann die folgenden telecine-Attribute an die übermittelt Medien Beispiele anfügen.</span><span class="sxs-lookup"><span data-stu-id="4c317-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="4c317-152">Attribut</span><span class="sxs-lookup"><span data-stu-id="4c317-152">Attribute</span></span>                                                                                   | <span data-ttu-id="4c317-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c317-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="4c317-154">**MF Sample Extension \_ repeatfirstfield**</span><span class="sxs-lookup"><span data-stu-id="4c317-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="4c317-155">Entspricht dem Flag "Repeat First Field" (RFF).</span><span class="sxs-lookup"><span data-stu-id="4c317-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="4c317-156">**MF Sample Extension \_ bottomfieldfirst**</span><span class="sxs-lookup"><span data-stu-id="4c317-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="4c317-157">Umgekehrter Wert für das Flag "Top Field First" (tff).</span><span class="sxs-lookup"><span data-stu-id="4c317-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="4c317-158">Diese Flags stellen einen Hinweis für den erweiterten Videorenderer (EVR) dar, wenn Sie Deinterlacing ausführt.</span><span class="sxs-lookup"><span data-stu-id="4c317-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="4c317-159">Ein Decoder sollte diese Flags nach unten weitergeben, indem Sie Sie in die Ausgabe Beispiele kopieren, damit Sie den EVR erreichen.</span><span class="sxs-lookup"><span data-stu-id="4c317-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c317-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c317-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c317-161">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="4c317-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
