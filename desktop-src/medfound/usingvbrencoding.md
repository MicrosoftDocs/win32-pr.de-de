---
description: In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Verwenden der VBR-Codierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215002"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="011cd-103">Verwenden der VBR-Codierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="011cd-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="011cd-104">Wie im Thema [Codierungs Methoden](encodingmethods.md) ausführlich beschrieben, wird die Codierung der Variablen Bitrate (VBR) verwendet, um die Konsistenz der Inhaltsqualität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="011cd-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="011cd-105">Sie konfigurieren VBR-Streams auf die gleiche Weise, wie Sie die konstanten Bitrate (CBR)-Streams mit Ausnahme der Puffer Parameter (Bitrate und Puffer Fenster) codieren.</span><span class="sxs-lookup"><span data-stu-id="011cd-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="011cd-106">In diesem Abschnitt wird beschrieben, wie VBR-Streams konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="011cd-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="011cd-107">Konfigurieren von Qualitäts basierter VBR</span><span class="sxs-lookup"><span data-stu-id="011cd-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="011cd-108">Bei der Codierung mit der Qualitäts basierten VBR-Methode sind keine vordefinierten Puffer Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="011cd-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="011cd-109">Stattdessen geben Sie eine Qualitätsstufe (von 0 bis 100) an, die der Encoder verwendet, um die entsprechenden Puffer Parameter dynamisch zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="011cd-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="011cd-110">Dieser Codierungs Modus verwendet nur einen Codierungs Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="011cd-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="011cd-111">Sie können die unterstützten Qualitäts basierten VBR-Ausgabetypen für die Audiocodecs auflisten.</span><span class="sxs-lookup"><span data-stu-id="011cd-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="011cd-112">Sie müssen einen der Typen verwenden, die vom DMO beim Festlegen des Ausgabe Typs zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="011cd-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="011cd-113">Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="011cd-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="011cd-114">Um einen Qualitäts basierten VBR-Videostream zu konfigurieren, müssen Sie die Eigenschaften festlegen, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="011cd-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="011cd-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="011cd-115">Property</span></span>                                            | <span data-ttu-id="011cd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="011cd-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="011cd-117">mfpkey \_ vbrenabled</span><span class="sxs-lookup"><span data-stu-id="011cd-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="011cd-118">Auf Variant true festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="011cd-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="011cd-119">mfpkey \_ vbrquality</span><span class="sxs-lookup"><span data-stu-id="011cd-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="011cd-120">Legen Sie auf den gewünschten Qualitäts Wert von 0 bis 100 fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="011cd-121">Nicht alle Qualitätswerte stellen diskrete Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="011cd-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="011cd-122">Weitere Informationen finden Sie in der Eigenschafts Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="011cd-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="011cd-123">Konfigurieren von nicht eingeschränktem VBR</span><span class="sxs-lookup"><span data-stu-id="011cd-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="011cd-124">Bei der nicht eingeschränkten VBR-Codierung kann der Encoder die Größe einzelner Stichproben ohne explizite Puffer Limits variieren.</span><span class="sxs-lookup"><span data-stu-id="011cd-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="011cd-125">Die durchschnittliche Bitrate für die Dauer des resultierenden Inhalts muss jedoch kleiner oder gleich dem angegebenen Wert sein.</span><span class="sxs-lookup"><span data-stu-id="011cd-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="011cd-126">Für den uneingeschränkten VBR sind zwei Codierungs Überläufen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="011cd-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="011cd-127">Sie können die unterstützten zwei-Pass-VBR-Ausgabetypen für die Audiocodecs auflisten.</span><span class="sxs-lookup"><span data-stu-id="011cd-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="011cd-128">Sie müssen einen der Typen verwenden, die vom DMO beim Festlegen des Ausgabe Typs zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="011cd-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="011cd-129">Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="011cd-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="011cd-130">Um einen unbeschränkten VBR-Videostream zu konfigurieren, müssen Sie die Eigenschaften festlegen, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="011cd-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="011cd-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="011cd-131">Property</span></span>                                            | <span data-ttu-id="011cd-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="011cd-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="011cd-133">mfpkey \_ vbrenabled</span><span class="sxs-lookup"><span data-stu-id="011cd-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="011cd-134">Auf Variant true festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="011cd-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="011cd-135">mfpkey- \_ passesused</span><span class="sxs-lookup"><span data-stu-id="011cd-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="011cd-136">Legen Sie auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="011cd-137">mfpkey \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="011cd-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="011cd-138">Legen Sie auf die gewünschte durchschnittliche Bitrate fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="011cd-139">Konfigurieren von Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="011cd-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="011cd-140">VBR mit hoher Einschränkung ist so ähnlich wie der eingeschränkte VBR, da es sich auf eine durchschnittliche Bitrate während der Dauer des Streams beschränkt.</span><span class="sxs-lookup"><span data-stu-id="011cd-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="011cd-141">Darüber hinaus entspricht VBR mit hoher Einschränkung einem Spitzen Puffer.</span><span class="sxs-lookup"><span data-stu-id="011cd-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="011cd-142">Dieser Puffer wird mit einer Spitzen Bitrate und einem Spitzen Puffer Fenster beschrieben, ebenso wie ein CBR-Puffer durch eine durchschnittliche Bitrate und ein Puffer Fenster beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="011cd-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="011cd-143">Dieser Modus bietet dem Encoder Flexibilität bei der Codierung einzelner Beispiele, während die Spitzen Grenzen einhalten.</span><span class="sxs-lookup"><span data-stu-id="011cd-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="011cd-144">Dies ist besonders nützlich, wenn die Decodierung von einem Chip in einem Gerät durchgeführt wird, wie z. b. bei einem DVD-Player, bei dem Hardware Einschränkungen berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="011cd-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="011cd-145">Die unterstützten leistungsstarken VBR-Audioencoder-Ausgabetypen sind dieselben Typen, die für den nicht eingeschränkten VBR aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="011cd-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="011cd-146">Legen Sie die Spitzenwerte für den DMO fest, und verwenden Sie den übermittelten Typ.</span><span class="sxs-lookup"><span data-stu-id="011cd-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="011cd-147">Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="011cd-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="011cd-148">Zum Konfigurieren eines VBR-Videostreams mit hoher Größe müssen Sie die in der folgenden Tabelle aufgeführten Eigenschaften mithilfe der **IPropertyBag:: Write** -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="011cd-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="011cd-149">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="011cd-149">Property</span></span>                                            | <span data-ttu-id="011cd-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="011cd-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="011cd-151">mfpkey \_ vbrenabled</span><span class="sxs-lookup"><span data-stu-id="011cd-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="011cd-152">Auf Variant true festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="011cd-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="011cd-153">mfpkey- \_ passesused</span><span class="sxs-lookup"><span data-stu-id="011cd-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="011cd-154">Legen Sie auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="011cd-155">mfpkey \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="011cd-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="011cd-156">Legen Sie auf die gewünschte durchschnittliche Bitrate fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="011cd-157">mfpkey- \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="011cd-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="011cd-158">Legen Sie auf die gewünschte Spitzen Bitrate fest.</span><span class="sxs-lookup"><span data-stu-id="011cd-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="011cd-159">mfpkey ( \_ bmax)</span><span class="sxs-lookup"><span data-stu-id="011cd-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="011cd-160">Wird auf das Puffer Fenster festgelegt, das der Spitzen Bitrate entspricht.</span><span class="sxs-lookup"><span data-stu-id="011cd-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="011cd-161">Es wird empfohlen, die Spitzen Bitrate auf mindestens doppelte die durchschnittliche Bitrate festzulegen.</span><span class="sxs-lookup"><span data-stu-id="011cd-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="011cd-162">Das Festlegen der Spitzen Rate auf einen niedrigeren Wert kann bewirken, dass der Codec den Inhalt als zwei-Pass-CBR anstelle von VBR mit eingeschränkter Spitzen Codierung codiert.</span><span class="sxs-lookup"><span data-stu-id="011cd-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="011cd-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="011cd-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="011cd-164">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="011cd-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="011cd-165">Verwenden von Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="011cd-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="011cd-166">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="011cd-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="011cd-167">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="011cd-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



