---
description: Encoder-Schnittstellen
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Encoder-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216818"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="fb3ad-103">Encoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fb3ad-103">Encoder Interfaces</span></span>


<span data-ttu-id="fb3ad-104">In den folgenden Tabellen sind die von Windows Imaging Component (WIC)-Encodern implementierten Schnittstellen aufgeführt, und das Klassendiagramm zeigt die Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="fb3ad-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="fb3ad-105">Container-Level Encoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fb3ad-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="fb3ad-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fb3ad-106">Interface</span></span>                                                                                       | <span data-ttu-id="fb3ad-107">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="fb3ad-107">Responsibilities</span></span>                             | <span data-ttu-id="fb3ad-108">Implementierung</span><span class="sxs-lookup"><span data-stu-id="fb3ad-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="fb3ad-109">Iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="fb3ad-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="fb3ad-110">Dienste auf Container Ebene</span><span class="sxs-lookup"><span data-stu-id="fb3ad-110">Container-level services</span></span>                     | <span data-ttu-id="fb3ad-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb3ad-111">Required</span></span>                                                                   |
| [<span data-ttu-id="fb3ad-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="fb3ad-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="fb3ad-113">Unterstützung für die Fortschritts Benachrichtigung & Abbruch</span><span class="sxs-lookup"><span data-stu-id="fb3ad-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="fb3ad-114">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="fb3ad-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="fb3ad-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="fb3ad-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="fb3ad-116">Dienste für die metadatenserialisierung</span><span class="sxs-lookup"><span data-stu-id="fb3ad-116">Metadata serialization services</span></span>              | <span data-ttu-id="fb3ad-117">Optional (nur für Formate erforderlich, die Metadaten auf Container Ebene unterstützen)</span><span class="sxs-lookup"><span data-stu-id="fb3ad-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="fb3ad-118">Frame-Level Encoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fb3ad-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="fb3ad-119">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fb3ad-119">Interface</span></span>                                                       | <span data-ttu-id="fb3ad-120">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="fb3ad-120">Responsibilities</span></span>                | <span data-ttu-id="fb3ad-121">Implementierung</span><span class="sxs-lookup"><span data-stu-id="fb3ad-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="fb3ad-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="fb3ad-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="fb3ad-123">Dienste auf Frame-Ebene</span><span class="sxs-lookup"><span data-stu-id="fb3ad-123">Frame-level services</span></span>            | <span data-ttu-id="fb3ad-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb3ad-124">Required</span></span>       |
| [<span data-ttu-id="fb3ad-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="fb3ad-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="fb3ad-126">Dienste für die metadatenserialisierung</span><span class="sxs-lookup"><span data-stu-id="fb3ad-126">Metadata serialization services</span></span> | <span data-ttu-id="fb3ad-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb3ad-127">Required</span></span>       |



 

![Vererbungs Hierarchie der WIC-Codierer](graphics/wicencoderinterfaces.png)

<span data-ttu-id="fb3ad-129">Sie werden bemerken, dass es sich bei den Codierungs Schnittstellen fast um Spiegelbilder der Decoder-Schnittstellen handelt und dass die meisten Methoden dieser Schnittstellen Methoden auf den zugehörigen Decoder-Schnittstellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fb3ad-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="fb3ad-130">Nachdem Sie nun mit der Implementierung eines WIC-fähigen Decoders vertraut sind, wird die Implementierung eines WIC-fähigen Encoders ebenfalls vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="fb3ad-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb3ad-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb3ad-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fb3ad-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="fb3ad-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fb3ad-133">Implementieren eines WIC-Enabled Encoders</span><span class="sxs-lookup"><span data-stu-id="fb3ad-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="fb3ad-134">Implementieren von iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="fb3ad-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="fb3ad-135">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="fb3ad-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="fb3ad-136">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="fb3ad-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



