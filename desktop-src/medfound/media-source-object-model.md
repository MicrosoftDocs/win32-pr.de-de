---
description: Medienquellen-Objektmodell
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Medienquellen-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351529"
---
# <a name="media-source-object-model"></a><span data-ttu-id="0487a-103">Medienquellen-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="0487a-103">Media Source Object Model</span></span>

<span data-ttu-id="0487a-104">In diesem Thema wird das Objektmodell für Medienquellen in Microsoft Media Foundation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0487a-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="0487a-105">Eine Medienquelle muss zwei Objekte implementieren:</span><span class="sxs-lookup"><span data-stu-id="0487a-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="0487a-106">Ein Präsentations Deskriptor, der den Inhalt der Quelle beschreibt, einschließlich der Anzahl der Streams und des Formats der einzelnen Datenströme.</span><span class="sxs-lookup"><span data-stu-id="0487a-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="0487a-107">Weitere Informationen zu Präsentations Deskriptoren finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="0487a-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="0487a-108">Ein oder mehrere Mediendaten Ströme, die die Quelldaten generieren.</span><span class="sxs-lookup"><span data-stu-id="0487a-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="0487a-109">Die Quelle erstellt die Streams erst, wenn die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0487a-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="0487a-110">Medienquellen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0487a-110">Media Source Interfaces</span></span>

<span data-ttu-id="0487a-111">Eine Medienquelle muss die folgenden Schnittstellen über **QueryInterface** verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0487a-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="0487a-112">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0487a-112">Interface</span></span>                                                | <span data-ttu-id="0487a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0487a-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0487a-114">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="0487a-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="0487a-115">Für alle Medienquellen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0487a-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="0487a-116">**IMF Media Event Generator**</span><span class="sxs-lookup"><span data-stu-id="0487a-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="0487a-117">Für alle Medienquellen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0487a-117">Required for all media sources.</span></span> <span data-ttu-id="0487a-118">Die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle erbt diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0487a-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="0487a-119">Optional kann eine Medienquelle die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle implementieren und eine der folgenden Schnittstellen als Dienste implementieren:</span><span class="sxs-lookup"><span data-stu-id="0487a-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="0487a-120">Dienst Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0487a-120">Service interface</span></span>                                  | <span data-ttu-id="0487a-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0487a-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="0487a-122">**Imfratecontrol**</span><span class="sxs-lookup"><span data-stu-id="0487a-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="0487a-123">Steuert die Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="0487a-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="0487a-124">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="0487a-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="0487a-125">Meldet den Bereich von Wiedergabe Raten, die unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0487a-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="0487a-126">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="0487a-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="0487a-127">Ermöglicht es dem Quality Manager, die Audioqualität oder Videoqualität anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0487a-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="0487a-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="0487a-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="0487a-129">Stellt Metadaten bereit.</span><span class="sxs-lookup"><span data-stu-id="0487a-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="0487a-130">Wenn die Medienquelle bei anderen raten als normaler Geschwindigkeit (1,0) wiedergegeben werden kann, sollte Sie den Raten Steuerungs Dienst ("[**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) " und " [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)") verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0487a-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="0487a-131">Andernfalls wird davon ausgegangen, dass die Quelle nur die Wiedergabe mit normaler Geschwindigkeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0487a-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="0487a-132">Weitere Informationen finden Sie unter [Implementieren der Raten Kontrolle](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="0487a-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="0487a-133">Weitere Informationen zu Dienst Schnittstellen und [**immagetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)finden Sie unter [Dienst Schnittstellen](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0487a-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="0487a-134">Medienstrom Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0487a-134">Media Stream Interfaces</span></span>

<span data-ttu-id="0487a-135">Mediendaten Ströme müssen die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="0487a-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="0487a-136">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0487a-136">Interface</span></span>                                                | <span data-ttu-id="0487a-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0487a-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0487a-138">**IMF Media Stream**</span><span class="sxs-lookup"><span data-stu-id="0487a-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="0487a-139">Erforderlich für alle Mediendaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="0487a-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="0487a-140">**IMF Media Event Generator**</span><span class="sxs-lookup"><span data-stu-id="0487a-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="0487a-141">Erforderlich für alle Mediendaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="0487a-141">Required for all media streams.</span></span> <span data-ttu-id="0487a-142">Die [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle erbt diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0487a-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="0487a-143">Zurzeit sind keine Dienst Schnittstellen für Mediendaten Ströme definiert.</span><span class="sxs-lookup"><span data-stu-id="0487a-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0487a-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0487a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0487a-145">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="0487a-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



