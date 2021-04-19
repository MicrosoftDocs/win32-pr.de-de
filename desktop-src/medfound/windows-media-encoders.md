---
description: Ein Encoder konvertiert unkomprimierte Audiodaten oder Videos in komprimierte Pakete in dem Format, das von der Anwendung angegeben wird. Zum Umrechnen von Mediendateien in das ASF-Format können Sie Windows Media-und Video Codecs verwenden.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354269"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="3a2db-104">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="3a2db-104">Windows Media Encoders</span></span>

<span data-ttu-id="3a2db-105">Ein Encoder konvertiert unkomprimierte Audiodaten oder Videos in komprimierte Pakete in dem Format, das von der Anwendung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a2db-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="3a2db-106">Zum Umrechnen von Mediendateien in das ASF-Format können Sie Windows Media-und Video Codecs verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a2db-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="3a2db-107">Ein Encoder wird durch die GUID identifiziert, die die Kategorie darstellt: Audiodaten oder Video.</span><span class="sxs-lookup"><span data-stu-id="3a2db-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="3a2db-108">Der Ausgabetyp des Encoders wird durch die Haupt-und Untertyp-GUID eines Medientyps dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3a2db-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="3a2db-109">Windows Media-Audiocodecs</span><span class="sxs-lookup"><span data-stu-id="3a2db-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="3a2db-110">Kategorie: **\_ \_ \_ Audioencoder der MFT-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="3a2db-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="3a2db-111">Haupttyp: MF MediaType \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="3a2db-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="3a2db-112">SubType: MF Audioformat \_ WMAudioV9, MF Audioformat \_ WMAudioV8, MF Audioformat \_ wmaudio \_ Lossless, MF Audioformat \_ wmaspdif</span><span class="sxs-lookup"><span data-stu-id="3a2db-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="3a2db-113">Windows Media-Video Codecs</span><span class="sxs-lookup"><span data-stu-id="3a2db-113">Windows Media video codecs</span></span>

    <span data-ttu-id="3a2db-114">Kategorie: **\_ \_ Video \_ Encoder der MFT-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="3a2db-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="3a2db-115">Haupttyp: MF MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="3a2db-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="3a2db-116">Untertyp: MF-Format \_ WVC1, MF-Format \_ WMV3, MF-Format \_ WMV2, MF-Format \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="3a2db-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="3a2db-117">Diese Encoder werden als [Media Foundation Transform](media-foundation-transforms.md) (MFT) implementiert, und Media Foundation ermöglicht den Zugriff auf die Anwendung über die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle des Encoder.</span><span class="sxs-lookup"><span data-stu-id="3a2db-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="3a2db-118">Wenn Sie Pipeline Schicht Komponenten für die ASF-Codierung verwenden, wird der Encoder-MFT als Transformations Knoten in die Pipeline eingefügt, da er für das Transformieren von Mediendaten verantwortlich ist, die durch die Quelle in die Senke fließen.</span><span class="sxs-lookup"><span data-stu-id="3a2db-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="3a2db-119">Wenn die Quelle ein komprimierter Typ ist, fügt die Pipeline die erforderlichen decoderer hinzu, um die Quelle in einen unkomprimierten Typ zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="3a2db-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="3a2db-120">Ein Encoder verfügt über einen Eingabestream und einen Ausgabestream.</span><span class="sxs-lookup"><span data-stu-id="3a2db-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="3a2db-121">Der Encoder empfängt Eingabedaten und erzeugt codierte Daten entsprechend der Konfiguration und dem Format, die von der Anwendung vor der Codierungs Sitzung festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="3a2db-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="3a2db-122">Das Format des Ausgabestreams wird durch einen Medientyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a2db-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="3a2db-123">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="3a2db-123">This section contains the following topics.</span></span>



| <span data-ttu-id="3a2db-124">Thema</span><span class="sxs-lookup"><span data-stu-id="3a2db-124">Topic</span></span>                                                                              | <span data-ttu-id="3a2db-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a2db-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a2db-126">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="3a2db-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="3a2db-127">Erläutert, wie der Encoder erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a2db-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="3a2db-128">Codierungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a2db-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="3a2db-129">Erläutert das Konfigurieren des Encoders durch Festlegen entsprechender Eigenschaften für den Encoder-MFT.</span><span class="sxs-lookup"><span data-stu-id="3a2db-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="3a2db-130">Medientyp Aushandlung für den Encoder</span><span class="sxs-lookup"><span data-stu-id="3a2db-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="3a2db-131">Erläutert, wie Eingabe-und Ausgabemedien Typen für den Encoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a2db-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="3a2db-132">Konfigurieren eines WMV-Encoders</span><span class="sxs-lookup"><span data-stu-id="3a2db-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="3a2db-133">Erläutert das Konfigurieren eines Windows Media Video-Encoders (WMV).</span><span class="sxs-lookup"><span data-stu-id="3a2db-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="3a2db-134">Festlegen eines Ausgabe Typs für einen WMA-Encoder</span><span class="sxs-lookup"><span data-stu-id="3a2db-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="3a2db-135">Erläutert, wie ein Ausgabetyp für einen Windows Media Audio (WMA)-Encoder festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3a2db-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="3a2db-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a2db-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2db-137">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="3a2db-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



