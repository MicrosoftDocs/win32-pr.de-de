---
title: Internet-Aware Objekte
description: Internet-Aware Objekte
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949161"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="ad042-103">Internet-Aware Objekte</span><span class="sxs-lookup"><span data-stu-id="ad042-103">Internet-Aware Objects</span></span>

<span data-ttu-id="ad042-104">Es wurden bestimmte Kategorien identifiziert, um die Persistenz-Schnittstellen abzudecken. Diese wurden durch Definieren der Funktionsweise von Steuerelementen über das Internet identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ad042-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="ad042-105">Ein Container, der den vollständigen Bereich der Persistenz-Schnittstellen nicht unterstützt, sollte sicherstellen, dass er kein Steuerelement hostet, das eine Kombination von Schnittstellen erfordert, die es nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad042-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="ad042-106">In den folgenden Tabellen wird die Bedeutung für verschiedene Kategorien sowohl als implementierte als auch als erforderliche Kategorien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad042-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="ad042-107">Erforderliche Kategorien</span><span class="sxs-lookup"><span data-stu-id="ad042-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="ad042-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad042-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad042-109">CATID \_ persiststomoniker, CATID \_ persiststostreaminit, CATID \_ persisitstostream, CATID \_ persiststostorage, CATID \_ persiststomemory, CATID \_ persiststofile, CATID \_ persiststopropertybag</span><span class="sxs-lookup"><span data-stu-id="ad042-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="ad042-110">Jede dieser Kategorien schließt sich gegenseitig aus und wird nur verwendet, wenn ein Objekt überhaupt nur einen Persistenzmechanismus unterstützt (also den gegenseitigen Ausschluss).</span><span class="sxs-lookup"><span data-stu-id="ad042-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="ad042-111">Container, die den Persistenzmechanismus nicht unterstützen, der in einer dieser Kategorien beschrieben wird, sollten das Erstellen von Objekten von Klassen verhindern, die als markiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad042-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="ad042-112">CATID "Requirements \_ sdatapathhost"</span><span class="sxs-lookup"><span data-stu-id="ad042-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="ad042-113">Das-Objekt erfordert die Möglichkeit, Daten in einem oder mehreren Pfaden zu speichern, und erfordert eine Container Beteiligung und erfordert daher Container Unterstützung für [**ibindhost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ad042-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="ad042-114">Implementierte Kategorien</span><span class="sxs-lookup"><span data-stu-id="ad042-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="ad042-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad042-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ad042-116">CATID \_ persiststomoniker, CATID \_ persiststostreaminit, CATID \_ persiststostream, CATID \_ persiststostorage, CATID \_ persiststomemory, CATID \_ persiststofile, CATID \_ persiststopropertybag</span><span class="sxs-lookup"><span data-stu-id="ad042-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="ad042-117">Object unterstützt den entsprechenden ipersistent- \* Mechanismus für die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="ad042-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="ad042-118">In der folgenden Tabelle werden die genauen CATIDs bereitstellt, die den einzelnen Kategorien zugewiesen sind:</span><span class="sxs-lookup"><span data-stu-id="ad042-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="ad042-119">Category</span><span class="sxs-lookup"><span data-stu-id="ad042-119">Category</span></span>                                | <span data-ttu-id="ad042-120">CATID</span><span class="sxs-lookup"><span data-stu-id="ad042-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="ad042-121">CATID "Requirements \_ sdatapathhost"</span><span class="sxs-lookup"><span data-stu-id="ad042-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="ad042-122">0un86a50-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-123">CATID \_ persiststomoniker</span><span class="sxs-lookup"><span data-stu-id="ad042-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="ad042-124">0un86a51-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-125">CATID \_ persiststostorage</span><span class="sxs-lookup"><span data-stu-id="ad042-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="ad042-126">0un86a52-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-127">CATID \_ persiststostreaminit</span><span class="sxs-lookup"><span data-stu-id="ad042-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="ad042-128">0un86a53-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-129">CATID \_ persiststostream</span><span class="sxs-lookup"><span data-stu-id="ad042-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="ad042-130">0un86a54-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-131">CATID \_ persiststomemory</span><span class="sxs-lookup"><span data-stu-id="ad042-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="ad042-132">0un86a55-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-133">CATID \_ persiststofile</span><span class="sxs-lookup"><span data-stu-id="ad042-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="ad042-134">0un86a56-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="ad042-135">CATID \_ persiststopropertybag</span><span class="sxs-lookup"><span data-stu-id="ad042-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="ad042-136">0un86a57-2baa-11CF-A229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="ad042-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ad042-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad042-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad042-138">Komponentenkategorien</span><span class="sxs-lookup"><span data-stu-id="ad042-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

