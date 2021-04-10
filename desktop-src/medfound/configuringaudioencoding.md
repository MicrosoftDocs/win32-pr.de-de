---
description: Konfigurieren der Audiocodierung
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Konfigurieren der Audiocodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214334"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="c6b44-103">Konfigurieren der Audiocodierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="c6b44-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="c6b44-104">Der Windows Media Audio Encoder listet alle unterstützten Ausgabetypen in seinem vollständigen Formular auf.</span><span class="sxs-lookup"><span data-stu-id="c6b44-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="c6b44-105">Rufen Sie den gewünschten Typ durch Aufrufen von **imediaobject:: getoutputtype** oder **imftransform:: getavailableoutputtype** ab, und legen Sie den abgerufenen Typ Unchanged als Ausgabetyp durch Aufrufen von **imediaobject:: setoutputtype** oder **imftransform:: setoutputtype** fest.</span><span class="sxs-lookup"><span data-stu-id="c6b44-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="c6b44-106">Die vom Audioencoder unterstützten Ausgabemedien Typen werden bei der Konfiguration der Codierungs Eigenschaften geändert.</span><span class="sxs-lookup"><span data-stu-id="c6b44-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="c6b44-107">Sie müssen alle Codierungs Eigenschaften konfigurieren, die Sie verwenden möchten, bevor Sie den Ausgabetyp auflisten.</span><span class="sxs-lookup"><span data-stu-id="c6b44-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="c6b44-108">Die Modi Two-Pass und VBR werden von den audioencodern unterstützt, sind jedoch anders konfiguriert als für Video.</span><span class="sxs-lookup"><span data-stu-id="c6b44-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="c6b44-109">Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="c6b44-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="c6b44-110">Die vom Audioencoder unterstützten Eingabetypen sind erst verfügbar, wenn Sie den Ausgabetyp festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="c6b44-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="c6b44-111">Wenn Sie **imediaobject:: getinputtype** oder **imftransform:: getinputtype** aufrufen, bevor Sie einen Ausgabetyp festlegen, gibt die Methode DMO \_ e \_ ohne \_ Weitere \_ Elemente \_ bzw. MFT e \_ nicht \_ mehr \_ Typen zurück.</span><span class="sxs-lookup"><span data-stu-id="c6b44-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="c6b44-112">Nachdem der Ausgabetyp festgelegt wurde, listet der Encoder die Eingabetypen auf, die er für den ausgewählten Ausgabetyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6b44-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="c6b44-113">Vom Windows Media Audio Encoder wird keine audioneu Stichprobe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6b44-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="c6b44-114">Dies bedeutet, dass der encoderausgabetyp und der codiereingabetyp die gleiche Anzahl von Kanälen, Bits pro Stichprobe und Stichprobenrate aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="c6b44-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="c6b44-115">Weitere Informationen finden Sie untersuchen von [Audioencoder-Ausgabetypen](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="c6b44-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="c6b44-116">Jeder vom Audioencoder aufgelistete Ausgabetyp enthält eine **WaveFormatEx** -Struktur (auf die von **am \_ Media \_ Type. pbformat** verwiesen wird), an die erweiterte Daten angehängt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6b44-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="c6b44-117">Die Größe der erweiterten Daten wird von **WaveFormatEx. cbSize** angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6b44-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="c6b44-118">Diese Daten müssen mit den codierten Inhalten aufbewahrt werden, damit Sie an den Decoder übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="c6b44-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="c6b44-119">Der Inhalt kann nicht ohne die erweiterten Formatierungsdaten dekomprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6b44-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c6b44-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6b44-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b44-121">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="c6b44-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



