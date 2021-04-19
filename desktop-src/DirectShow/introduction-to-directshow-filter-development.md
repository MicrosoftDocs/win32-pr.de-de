---
description: Einführung in die DirectShow-Filter Entwicklung
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Einführung in die DirectShow-Filter Entwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345396"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="6ad77-103">Einführung in die DirectShow-Filter Entwicklung</span><span class="sxs-lookup"><span data-stu-id="6ad77-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="6ad77-104">Dieser Abschnitt enthält eine kurze Übersicht über die Aufgaben, die bei der Entwicklung eines benutzerdefinierten DirectShow-Filters beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="6ad77-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="6ad77-105">Außerdem finden Sie hier Links zu Themen, in denen diese Aufgaben ausführlicher erörtert werden.</span><span class="sxs-lookup"><span data-stu-id="6ad77-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="6ad77-106">Lesen Sie vor dem Lesen dieses Abschnitts die Themen in [Informationen zu DirectShow](about-directshow.md), die die allgemeine DirectShow-Architektur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ad77-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="6ad77-107">**DirectShow-Basisklassen Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="6ad77-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="6ad77-108">Das DirectShow SDK enthält eine Reihe von C++-Klassen zum Schreiben von Filtern.</span><span class="sxs-lookup"><span data-stu-id="6ad77-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="6ad77-109">Obwohl Sie nicht erforderlich sind, sind diese Klassen die empfohlene Vorgehensweise zum Schreiben eines neuen Filters.</span><span class="sxs-lookup"><span data-stu-id="6ad77-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="6ad77-110">Wenn Sie die Basisklassen verwenden möchten, kompilieren Sie Sie in eine statische Bibliothek, und verknüpfen Sie die LIB-Datei mit dem Projekt, wie unter [Erstellen von DirectShow-Filtern](building-directshow-filters.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ad77-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="6ad77-111">Die Basisklassen Bibliothek definiert eine Stamm Klasse für Filter, die [**cbasefilter**](cbasefilter.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="6ad77-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="6ad77-112">Mehrere andere Klassen werden von **cbasefilter** abgeleitet und sind für bestimmte Arten von Filtern spezialisiert.</span><span class="sxs-lookup"><span data-stu-id="6ad77-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="6ad77-113">Beispielsweise ist die [**ctransformfilter**](ctransformfilter.md) -Klasse für Transformations Filter konzipiert.</span><span class="sxs-lookup"><span data-stu-id="6ad77-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="6ad77-114">Um einen neuen Filter zu erstellen, implementieren Sie eine Klasse, die von einer der Filterklassen erbt.</span><span class="sxs-lookup"><span data-stu-id="6ad77-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="6ad77-115">Die Klassen Deklaration könnte z. b. wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="6ad77-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="6ad77-116">Weitere Informationen zu den DirectShow-Basisklassen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6ad77-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="6ad77-117">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="6ad77-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="6ad77-118">Aufbauen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="6ad77-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="6ad77-119">**Erstellen von Pins**</span><span class="sxs-lookup"><span data-stu-id="6ad77-119">**Creating Pins**</span></span>

<span data-ttu-id="6ad77-120">Ein Filter muss mindestens einen Pins erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ad77-120">A filter must create one or more pins.</span></span> <span data-ttu-id="6ad77-121">Die Anzahl der Pins kann zur Entwurfszeit korrigiert werden, oder der Filter kann nach Bedarf neue Pins erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ad77-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="6ad77-122">Pins werden im Allgemeinen von der [**cbasepin**](cbasepin.md) -Klasse oder von einer Klasse abgeleitet, die **cbasepin** erbt, z. b. [**cbasinputpin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="6ad77-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="6ad77-123">Die Pins des Filters sollten als Element Variablen in der Filter-Klasse deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6ad77-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="6ad77-124">Einige der Filterklassen definieren bereits die Pins, aber wenn der Filter direkt von **cbasefilter** erbt, müssen Sie die Pins in der abgeleiteten Klasse deklarieren.</span><span class="sxs-lookup"><span data-stu-id="6ad77-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="6ad77-125">**Aushandeln von PIN-Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="6ad77-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="6ad77-126">Wenn der Filter Graph-Manager versucht, zwei Filter zu verbinden, müssen die Pins den verschiedenen Dingen zustimmen.</span><span class="sxs-lookup"><span data-stu-id="6ad77-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="6ad77-127">Wenn dies nicht möglich ist, schlägt der Verbindungsversuch fehl.</span><span class="sxs-lookup"><span data-stu-id="6ad77-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="6ad77-128">Im Allgemeinen werden bei Pins folgende Aushandlungen ausgehandelt:</span><span class="sxs-lookup"><span data-stu-id="6ad77-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="6ad77-129">Transport:</span><span class="sxs-lookup"><span data-stu-id="6ad77-129">Transport.</span></span> <span data-ttu-id="6ad77-130">Der Transport ist der Mechanismus, den die Filter zum Verschieben von Medien Beispielen aus der Ausgabe-PIN in die Eingabe-PIN verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ad77-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="6ad77-131">Sie können z. b. die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ("Push Model") oder die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle ("Pull Model") verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ad77-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="6ad77-132">Medientyp.</span><span class="sxs-lookup"><span data-stu-id="6ad77-132">Media type.</span></span> <span data-ttu-id="6ad77-133">Fast alle Pins verwenden Medientypen, um das Format der Daten zu beschreiben, die Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6ad77-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="6ad77-134">Allocator.</span><span class="sxs-lookup"><span data-stu-id="6ad77-134">Allocator.</span></span> <span data-ttu-id="6ad77-135">Die Zuweisung ist das Objekt, mit dem die Puffer erstellt werden, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="6ad77-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="6ad77-136">Die Pins müssen zustimmen, welche PIN die Zuweisung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6ad77-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="6ad77-137">Sie müssen außerdem die Größe der Puffer, die Anzahl der zu erstellenden Puffer und andere Puffer Eigenschaften akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6ad77-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="6ad77-138">Die Basisklassen implementieren ein Framework für diese Aushandlungen.</span><span class="sxs-lookup"><span data-stu-id="6ad77-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="6ad77-139">Sie müssen die Details vervollständigen, indem Sie verschiedene Methoden in der Basisklasse überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ad77-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="6ad77-140">Der Satz von Methoden, die Sie überschreiben müssen, hängt von der-Klasse und der Funktionalität des Filters ab.</span><span class="sxs-lookup"><span data-stu-id="6ad77-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="6ad77-141">Weitere Informationen finden Sie unter Gewusst [wie: Verbinden von Filtern](how-filters-connect.md).</span><span class="sxs-lookup"><span data-stu-id="6ad77-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="6ad77-142">**Verarbeiten und Bereitstellung von Daten**</span><span class="sxs-lookup"><span data-stu-id="6ad77-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="6ad77-143">Die Hauptfunktion der meisten Filter ist die Verarbeitung und Bereitstellung von Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="6ad77-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="6ad77-144">Wie dies geschieht, hängt vom Filtertyp ab:</span><span class="sxs-lookup"><span data-stu-id="6ad77-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="6ad77-145">Eine Push-Quelle verfügt über einen Arbeits Thread, der kontinuierlich Stichproben mit Daten füllt und diese nach unten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6ad77-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="6ad77-146">Eine Pull-Quelle wartet darauf, dass der Downstream-Nachbar ein Beispiel anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ad77-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="6ad77-147">Er antwortet, indem er Daten in ein Beispiel schreibt und das Beispiel für den downstreamfilter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6ad77-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="6ad77-148">Der Downstream-Filter erstellt den Thread, der den Datenfluss steuert.</span><span class="sxs-lookup"><span data-stu-id="6ad77-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="6ad77-149">Ein Transformations Filter enthält Beispiele, die von seinem upstreamnachbar bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ad77-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="6ad77-150">Wenn ein Beispiel empfangen wird, werden die Daten verarbeitet und nachgelagert.</span><span class="sxs-lookup"><span data-stu-id="6ad77-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="6ad77-151">Ein rendererfilter empfängt Beispiele von Upstream und plant das Rendering basierend auf den Zeitstempeln.</span><span class="sxs-lookup"><span data-stu-id="6ad77-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="6ad77-152">Andere Aufgaben im Zusammenhang mit dem Streaming umfassen das Leeren von Daten aus dem Diagramm, das Verarbeiten des Datenstroms und das reagieren auf Suchanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ad77-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="6ad77-153">Weitere Informationen zu diesen Problemen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6ad77-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="6ad77-154">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="6ad77-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="6ad77-155">Qualitäts Steuerungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="6ad77-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="6ad77-156">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="6ad77-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="6ad77-157">**Unterstützendes com**</span><span class="sxs-lookup"><span data-stu-id="6ad77-157">**Supporting COM**</span></span>

<span data-ttu-id="6ad77-158">DirectShow-Filter sind COM-Objekte, die in der Regel in DLLs verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="6ad77-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="6ad77-159">Die Basisklassen Bibliothek implementiert ein Framework für die Unterstützung von com.</span><span class="sxs-lookup"><span data-stu-id="6ad77-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="6ad77-160">Dies wird im Abschnitt [DirectShow und com](directshow-and-com.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ad77-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ad77-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ad77-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ad77-162">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="6ad77-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



