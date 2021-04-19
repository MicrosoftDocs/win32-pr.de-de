---
description: Die crendererpospassthru-Klasse verarbeitet Such Befehle für rendererfilter, indem Sie vom Upstream an den nächsten Filter übergeben werden.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Crendererpospassthru-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360399"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="bb421-103">Crendererpospassthru-Klasse</span><span class="sxs-lookup"><span data-stu-id="bb421-103">CRendererPosPassThru class</span></span>

![crendererpospassthru-Klassenhierarchie](images/cutil14.png)

<span data-ttu-id="bb421-105">Die- `CRendererPosPassThru` Klasse verarbeitet Such Befehle für rendererfilter, indem Sie vom Upstream an den nächsten Filter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb421-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="bb421-106">Diese Klasse wird von der [**cpospassthru**](cpospassthru.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bb421-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="bb421-107">Es fügt Unterstützung für das Zwischenspeichern der Zeitstempel aus den Stichproben hinzu</span><span class="sxs-lookup"><span data-stu-id="bb421-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="bb421-108">Verwenden Sie diese Klasse auf die gleiche Weise wie die **cpospassthru** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bb421-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="bb421-109">Ausführliche Informationen finden Sie in der **cpospassthru** -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="bb421-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="bb421-110">Der rendererfilter muss die `CRendererPosPassThru` zwischengespeicherten Zeitstempel des Objekts wie folgt aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="bb421-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="bb421-111">Für jedes Beispiel, das der Filter empfängt, wird die [**crendererpospassthru:: registermediatime**](crendererpospassthru-registermediatime.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bb421-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="bb421-112">Wenn der Filter beendet wird oder einen **endflush** -Anruf empfängt, können Sie die [**crendererpospassthru:: resetmediatime**](crendererpospassthru-resetmediatime.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bb421-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="bb421-113">Wenn der Filter eine Benachrichtigung über das Ende des Datenstroms empfängt, wird die [**crendererpospassthru:: EOS**](crendererpospassthru-eos.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bb421-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="bb421-114">Ein Beispiel für die Verwendung dieser Klasse finden Sie unter [**cbaserenderer**](cbaserenderer.md) -Quellcode.</span><span class="sxs-lookup"><span data-stu-id="bb421-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="bb421-115">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="bb421-115">Public Methods</span></span>                                                            | <span data-ttu-id="bb421-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb421-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="bb421-117">**Crendererpospassthru**</span><span class="sxs-lookup"><span data-stu-id="bb421-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="bb421-118">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="bb421-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="bb421-119">**Getmediatime**</span><span class="sxs-lookup"><span data-stu-id="bb421-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="bb421-120">Ruft die Zeitstempel im aktuellen Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="bb421-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="bb421-121">**Registermediatime**</span><span class="sxs-lookup"><span data-stu-id="bb421-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="bb421-122">Speichert die Zeitstempel aus dem aktuellen Beispiel zwischen.</span><span class="sxs-lookup"><span data-stu-id="bb421-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="bb421-123">**Resetmediatime**</span><span class="sxs-lookup"><span data-stu-id="bb421-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="bb421-124">Setzt die zwischengespeicherten Zeitstempel auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="bb421-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="bb421-125">**Stereo**</span><span class="sxs-lookup"><span data-stu-id="bb421-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="bb421-126">Aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bb421-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bb421-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb421-127">Requirements</span></span>



| <span data-ttu-id="bb421-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb421-128">Requirement</span></span> | <span data-ttu-id="bb421-129">Wert</span><span class="sxs-lookup"><span data-stu-id="bb421-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb421-130">Header</span><span class="sxs-lookup"><span data-stu-id="bb421-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bb421-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb421-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb421-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb421-132">Library</span></span><br/> | <dl> <span data-ttu-id="bb421-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bb421-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




