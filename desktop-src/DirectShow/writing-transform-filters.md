---
description: Schreiben von Transformations Filtern
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Schreiben von Transformations Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959937"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="d3ac3-103">Schreiben von Transformations Filtern</span><span class="sxs-lookup"><span data-stu-id="d3ac3-103">Writing Transform Filters</span></span>

<span data-ttu-id="d3ac3-104">In diesem Abschnitt wird beschrieben, wie ein Transformations Filter geschrieben wird, der als Filter mit genau einer Eingabe-PIN und einer Ausgabe-PIN definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="d3ac3-105">Um die Schritte zu veranschaulichen, wird in diesem Abschnitt ein hypothetischer Transformations Filter beschrieben, der ein RLE-Video (Run-Length-codiert) ausgibt.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="d3ac3-106">Der RLE-Codierungs Algorithmus selbst wird nicht beschrieben, sondern nur die Aufgaben, die für DirectShow spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="d3ac3-107">(DirectShow stellt bereits einen RLE-Codec über den [AVI-Kompressor](avi-compressor-filter.md) -Filter bereit.)</span><span class="sxs-lookup"><span data-stu-id="d3ac3-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="d3ac3-108">In diesem Abschnitt wird davon ausgegangen, dass Sie die DirectShow-Basisklassen Bibliothek verwenden, um Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="d3ac3-109">Obwohl Sie einen Filter ohne diesen schreiben können, wird dringend empfohlen, die Basisklassen Bibliothek zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="d3ac3-110">Vor dem Schreiben eines Transformations Filters sollten Sie überprüfen, ob ein DirectX-Medienobjekt (DMO) Ihre Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="d3ac3-111">DMOS kann viele der gleichen Aufgaben wie Filter ausführen, und das Programmiermodell für DMOS ist einfacher.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="d3ac3-112">DMOS werden in DirectShow über den [DMO-Wrapper](dmo-wrapper-filter.md) Filter gehostet, können aber auch außerhalb von DirectShow verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="d3ac3-113">DMOS sind nun die empfohlene Lösung für Encoder und Decoders.</span><span class="sxs-lookup"><span data-stu-id="d3ac3-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="d3ac3-114">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="d3ac3-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="d3ac3-115">Schritt 1: Basisklasse auswählen</span><span class="sxs-lookup"><span data-stu-id="d3ac3-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="d3ac3-116">Schritt 2: Deklarieren der Filter Klasse</span><span class="sxs-lookup"><span data-stu-id="d3ac3-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="d3ac3-117">Schritt 3. Unterstützung der Medientyp Aushandlung</span><span class="sxs-lookup"><span data-stu-id="d3ac3-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="d3ac3-118">Schritt 4: Festlegen von zuordnereigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3ac3-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="d3ac3-119">Schritt 5: Transformieren des Bilds</span><span class="sxs-lookup"><span data-stu-id="d3ac3-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="d3ac3-120">Schritt 6: Unterstützung für com hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d3ac3-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="d3ac3-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3ac3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3ac3-122">Aufbauen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="d3ac3-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d3ac3-123">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="d3ac3-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="d3ac3-124">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="d3ac3-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



