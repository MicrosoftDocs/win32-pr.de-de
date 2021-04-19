---
description: Die cbaserendererinputpin-Klasse implementiert eine Eingabe-PIN für die cbasererererklasse. Sofern nicht angegeben, werden die Methoden in dieser Klasse an die entsprechenden Methoden der cbasererererklasse delegiert.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Crendererinputpin-Klasse (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358786"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="0d6a1-104">Crendererinputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d6a1-104">CRendererInputPin class</span></span>

![crendererinput-Pin-Klassenhierarchie](images/rbase01.png)

<span data-ttu-id="0d6a1-106">Die **cbaserendererinputpin** -Klasse implementiert eine Eingabe-PIN für die [**cbasererererklasse**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="0d6a1-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="0d6a1-107">Sofern nicht angegeben, werden die Methoden in dieser Klasse an die entsprechenden Methoden der **cbasererererklasse** delegiert.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="0d6a1-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="0d6a1-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="0d6a1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d6a1-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d6a1-110">**m- \_ prenderer**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="0d6a1-111">Zeiger auf den Filter.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="0d6a1-112">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="0d6a1-112">Public Methods</span></span>                                                   | <span data-ttu-id="0d6a1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d6a1-113">Description</span></span>                                                                            |
| [<span data-ttu-id="0d6a1-114">**Crendererinputpin**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="0d6a1-115">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="0d6a1-116">**Breakconnect**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="0d6a1-117">Fügt beim Abbrechen einer Verbindung angepassten Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="0d6a1-118">**Completeconnect**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="0d6a1-119">Schließt die Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="0d6a1-120">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="0d6a1-121">Bestimmt, ob die PIN einen bestimmten Medientyp unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="0d6a1-122">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="0d6a1-123">Schaltet die PIN in den aktiven (angehaltenen oder laufenden) Modus.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="0d6a1-124">**Inaktiv**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="0d6a1-125">Schaltet die PIN in einen inaktiven Zustand und gibt den Speicher der Zuweisung frei.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="0d6a1-126">**Setmediatype**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="0d6a1-127">Legt den Medientyp der PIN fest.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="0d6a1-128">**Allocator**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="0d6a1-129">Ruft einen Zeiger auf die Standard Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="0d6a1-130">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="0d6a1-130">IPin Methods</span></span>                                                     | <span data-ttu-id="0d6a1-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d6a1-131">Description</span></span>                                                                            |
| [<span data-ttu-id="0d6a1-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="0d6a1-133">Ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="0d6a1-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="0d6a1-135">Teilt der PIN mit, dass keine weiteren Daten erwartet werden, bis ein neuer Befehl zum Ausführen ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="0d6a1-136">**Beginflush**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="0d6a1-137">Teilt der PIN mit, einen Leerungs Vorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="0d6a1-138">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="0d6a1-139">Teilt der PIN mit, einen Leerungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="0d6a1-140">IMemInputPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="0d6a1-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="0d6a1-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d6a1-141">Description</span></span>                                                                            |
| [<span data-ttu-id="0d6a1-142">**Medizinisch**</span><span class="sxs-lookup"><span data-stu-id="0d6a1-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="0d6a1-143">Ruft den nächsten Datenblock aus dem Stream ab.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="0d6a1-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d6a1-144">Requirements</span></span>



| <span data-ttu-id="0d6a1-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d6a1-145">Requirement</span></span> | <span data-ttu-id="0d6a1-146">Wert</span><span class="sxs-lookup"><span data-stu-id="0d6a1-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6a1-147">Header</span><span class="sxs-lookup"><span data-stu-id="0d6a1-147">Header</span></span><br/>  | <dl> <span data-ttu-id="0d6a1-148"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a1-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0d6a1-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d6a1-149">Library</span></span><br/> | <dl> <span data-ttu-id="0d6a1-150">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a1-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




