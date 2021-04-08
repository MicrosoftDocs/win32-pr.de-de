---
description: Verwenden von Medienquellen mit der Medien Sitzung
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Verwenden von Medienquellen mit der Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961138"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="f169c-103">Verwenden von Medienquellen mit der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="f169c-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="f169c-104">Wenn Sie die Medien Sitzung zum Steuern der Wiedergabe verwenden, ist der Satz von Methoden, den Sie für eine Medienquelle aufzurufen sollten, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f169c-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="f169c-105">In diesem Abschnitt wird beschrieben, wie Medienquellen in Verbindung mit der Medien Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f169c-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="f169c-106">Im folgenden finden Sie die grundlegenden Schritte, die Ihre Anwendung ausführt:</span><span class="sxs-lookup"><span data-stu-id="f169c-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="f169c-107">Erstellen Sie die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="f169c-107">Create the media source.</span></span> <span data-ttu-id="f169c-108">Verwenden Sie zum Erstellen einer Medienquelle den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="f169c-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="f169c-109">Weitere Informationen finden Sie unter [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="f169c-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="f169c-110">Der quellresolver gibt einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Quelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f169c-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="f169c-111">(Wenn Sie eine benutzerdefinierte Medienquelle geschrieben haben, können Sie stattdessen eine benutzerdefinierte Erstellungs Methode bereitstellen.)</span><span class="sxs-lookup"><span data-stu-id="f169c-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="f169c-112">Konfigurieren Sie die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="f169c-112">Configure the presentation.</span></span> <span data-ttu-id="f169c-113">Um die Darstellung der Quelle zu konfigurieren, müssen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f169c-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="f169c-114">Sie können diese Kopie ändern, aber die Änderungen werden erst nach dem Start der Wiedergabe aktiv.</span><span class="sxs-lookup"><span data-stu-id="f169c-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="f169c-115">Ändern Sie den Präsentations Deskriptor während der Wiedergabe nicht.</span><span class="sxs-lookup"><span data-stu-id="f169c-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="f169c-116">Weitere Informationen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="f169c-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="f169c-117">Erstellen Sie eine Topologie, die die Medienquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="f169c-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="f169c-118">Weitere Informationen finden Sie unter [Topologien](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="f169c-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="f169c-119">Verwenden Sie die Medien Sitzung zum Steuern der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="f169c-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="f169c-120">In der Medien Sitzung werden Methoden für die Medienquelle aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f169c-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="f169c-121">Die Anwendung sollte zu diesem Zeitpunkt keine Methoden für die Medienquelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="f169c-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="f169c-122">Bevor Sie die Medienquelle freigeben, wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Quelle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="f169c-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="f169c-123">Wenn Sie die Sequencer-Quelle verwenden, verarbeitet die Sequencer-Quelle das Herunterfahren der Segment Quellen.</span><span class="sxs-lookup"><span data-stu-id="f169c-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="f169c-124">Weitere Informationen finden Sie unter [Sequencer-Quelle](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="f169c-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="f169c-125">Wenn Sie die Medien Sitzung verwenden, sind die einzigen Methoden, die Sie für die Medienquelle aufrufen sollten, " [**kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)", " [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)" und " [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)".</span><span class="sxs-lookup"><span data-stu-id="f169c-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="f169c-126">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="f169c-126">In particular:</span></span>

-   <span data-ttu-id="f169c-127">" [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)", " [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)" oder " [**Anhalten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop)" nicht aufzurufen. Diese Methoden sollten nur von der Medien Sitzung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f169c-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="f169c-128">Es werden keine [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Methoden aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f169c-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="f169c-129">Rufen Sie keine Ereignisse direkt aus der Medienquelle oder einem der Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f169c-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="f169c-130">Die Medien Sitzung muss diese Ereignisse empfangen, damit die Pipeline ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f169c-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="f169c-131">Die Medien Sitzung leitet alle Ereignisse weiter, die von der Anwendung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f169c-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f169c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f169c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f169c-133">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="f169c-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



