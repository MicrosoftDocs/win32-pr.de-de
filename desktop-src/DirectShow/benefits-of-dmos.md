---
description: Vorteile von dmos
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vorteile von dmos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213964"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="39363-103">Vorteile von dmos</span><span class="sxs-lookup"><span data-stu-id="39363-103">Benefits of DMOs</span></span>

<span data-ttu-id="39363-104">DMOS bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="39363-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="39363-105">Sie sind im Allgemeinen kleiner und einfacher als DirectShow-Filter, da Sie weniger Funktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39363-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="39363-106">Sie sind flexibler als DirectShow-Filter, da Sie kein Filter Diagramm benötigen.</span><span class="sxs-lookup"><span data-stu-id="39363-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="39363-107">Sie können Sie mit DirectShow verwenden, wenn Sie die von DirectShow bereitgestellten Dienste benötigen, z. b. Synchronisierung, intelligente Verbindung, automatische Verarbeitung des Datenflusses und Thread Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="39363-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="39363-108">Clients, die diese Dienste nicht benötigen, können direkt auf DMOS zugreifen.</span><span class="sxs-lookup"><span data-stu-id="39363-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="39363-109">DMOS führt immer eine synchrone Datenverarbeitung durch, wodurch viele der Threading Probleme vermieden werden, die Sie beim Schreiben eines Filters beachten müssen.</span><span class="sxs-lookup"><span data-stu-id="39363-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="39363-110">Im Gegensatz zu herkömmlichen ACM-und VCM-Codecs basieren DMOS auf dem Component Object Model (com), sodass Sie über **QueryInterface** erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="39363-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="39363-111">DMOS unterstützen ein generalisiertes Streamingmodell als ACM-oder VCM-Codecs.</span><span class="sxs-lookup"><span data-stu-id="39363-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="39363-112">Wie DirectShow-Filter kann DMOS mehrere Eingaben und mehrere Ausgaben unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39363-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="39363-113">Aus diesen Gründen werden DMOS nun als Lösung für das Schreiben von Encodern, Decodern und Audioeffekten empfohlen.</span><span class="sxs-lookup"><span data-stu-id="39363-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="39363-114">Viele andere Szenarien sind auch möglich, abhängig von den Anforderungen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="39363-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="39363-115">Unterschiede zwischen DMOS und DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="39363-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="39363-116">DirectShow-Filter können nicht außerhalb eines DirectShow-Filter Diagramms funktionieren.</span><span class="sxs-lookup"><span data-stu-id="39363-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="39363-117">In DirectShow wird der Filter Graph-Manager zwischen der Anwendung und den Filtern mediiert.</span><span class="sxs-lookup"><span data-stu-id="39363-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="39363-118">DirectShow-Filter führen den größten Teil der Arbeit aus, die zum Streamen von Daten erforderlich ist, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="39363-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="39363-119">Puffer werden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="39363-119">Allocating buffers.</span></span>
-   <span data-ttu-id="39363-120">Aushandeln von Medientypen und Verbindungen mit anderen Filtern.</span><span class="sxs-lookup"><span data-stu-id="39363-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="39363-121">Übertragen von Daten über das Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="39363-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="39363-122">Senden von Ereignissen an den Filter Diagramm-Manager.</span><span class="sxs-lookup"><span data-stu-id="39363-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="39363-123">Synchronisieren mehrerer Threads.</span><span class="sxs-lookup"><span data-stu-id="39363-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="39363-124">Im Gegensatz dazu führt ein DMO keines dieser Dinge aus.</span><span class="sxs-lookup"><span data-stu-id="39363-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="39363-125">Stattdessen sind diese Arten von Aufgaben für den Client mit dem DMO verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="39363-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="39363-126">Der Client ordnet Puffer zu, füllt sie mit Daten und übergibt sie an den DMO.</span><span class="sxs-lookup"><span data-stu-id="39363-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="39363-127">Der DMO verarbeitet die Daten, und der Client ruft die resultierenden Ausgabepuffer ab.</span><span class="sxs-lookup"><span data-stu-id="39363-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39363-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39363-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39363-129">Informationen zu DMOS</span><span class="sxs-lookup"><span data-stu-id="39363-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



