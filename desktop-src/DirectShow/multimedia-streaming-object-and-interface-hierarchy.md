---
description: Multimediastreamingobjekt und Schnittstellen Hierarchie
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Multimediastreamingobjekt und Schnittstellen Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869611"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="4fc29-103">Multimediastreamingobjekt und Schnittstellen Hierarchie</span><span class="sxs-lookup"><span data-stu-id="4fc29-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="4fc29-104">Diese APIs sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="4fc29-104">These APIs are deprecated.</span></span> <span data-ttu-id="4fc29-105">Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fc29-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="4fc29-106">Das folgende Diagramm zeigt die Objekthierarchie, die beim Multimedia-Streaming verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fc29-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![multimediastreaming-Objekthierarchie](images/mmstream02.png)

<span data-ttu-id="4fc29-108">Die Multimedia-streamingarchitektur definiert drei allgemeine Objekttyp:</span><span class="sxs-lookup"><span data-stu-id="4fc29-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="4fc29-109">Das **ammultimediastream** -Objekt macht die [**iammultimediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fc29-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="4fc29-110">Intern umschließt dieses Objekt das DirectShow-Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="4fc29-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="4fc29-111">*Media Stream* -Objekte machen die [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Schnittstelle verfügbar und sind Daten spezifisch.</span><span class="sxs-lookup"><span data-stu-id="4fc29-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="4fc29-112">Das ammultimediastream-Objekt enthält einen oder mehrere Mediendaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="4fc29-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="4fc29-113">*Stream-Beispiel* Objekte enthalten die Daten für einen bestimmten Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4fc29-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="4fc29-114">Die folgenden Medienstrom Objekte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4fc29-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="4fc29-115">Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="4fc29-115">Audio stream.</span></span> <span data-ttu-id="4fc29-116">Macht die [**iaudiomediastream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fc29-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="4fc29-117">DirectDraw-Stream.</span><span class="sxs-lookup"><span data-stu-id="4fc29-117">DirectDraw stream.</span></span> <span data-ttu-id="4fc29-118">Stellt einen Videostream dar, der auf eine DirectDraw-Oberfläche gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4fc29-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="4fc29-119">Macht die [**idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fc29-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="4fc29-120">Medientyp-Stream.</span><span class="sxs-lookup"><span data-stu-id="4fc29-120">Media type stream.</span></span> <span data-ttu-id="4fc29-121">Stellt beliebige Daten dar.</span><span class="sxs-lookup"><span data-stu-id="4fc29-121">Represents arbitrary data.</span></span> <span data-ttu-id="4fc29-122">Macht die [**iammediatypeer Stream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fc29-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="4fc29-123">Jedes Mediendaten Strom-Objekt erstellt eine eigene Art von Datenstrom Sample-Objekt:</span><span class="sxs-lookup"><span data-stu-id="4fc29-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="4fc29-124">Audiodatenströme erstellen Audiobeispiele, die die [**iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4fc29-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="4fc29-125">DirectDraw-Streams erstellen DirectDraw-Beispiele, die die [**idirectdrawstreamsample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4fc29-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="4fc29-126">Medientyp-Streams erstellen Beispiele für den Medientyp, die die [**iammediatypesample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4fc29-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="4fc29-127">Das folgende Diagramm zeigt die Schnittstellen Hierarchie für die zuvor aufgelisteten Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="4fc29-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![multimediastreaming-Schnittstellen Hierarchie](images/mmstream01.png)

 

 



