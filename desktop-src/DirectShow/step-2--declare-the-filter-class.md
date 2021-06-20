---
description: Deklarieren Sie eine C++-Klasse, die die Basisklasse erbt, die Sie beim Schreiben eines Transformationsfilters ausgewählt haben.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Schritt 2: Deklarieren der Filter-Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410063"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="2b8ed-104">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="2b8ed-104">Step 2.</span></span> <span data-ttu-id="2b8ed-105">Deklarieren der Filter-Klasse</span><span class="sxs-lookup"><span data-stu-id="2b8ed-105">Declare the Filter Class</span></span>

<span data-ttu-id="2b8ed-106">Dies ist Schritt 2 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2b8ed-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="2b8ed-107">Deklarieren Sie zunächst eine C++-Klasse, die die Basisklasse erbt:</span><span class="sxs-lookup"><span data-stu-id="2b8ed-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="2b8ed-108">Jeder Filterklasse sind Pinklassen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="2b8ed-109">Je nach den spezifischen Anforderungen Ihres Filters müssen Sie möglicherweise die Pin-Klassen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="2b8ed-110">Im Fall von **CTransformFilter** delegieren die Pins den Großteil ihrer Arbeit an den Filter, sodass Sie die Stecknadeln wahrscheinlich nicht überschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="2b8ed-111">Sie müssen eine eindeutige CLSID für den Filter generieren.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="2b8ed-112">Sie können das Hilfsprogramm Guidgen oder Uuidgen verwenden. Kopieren Sie niemals eine vorhandene GUID.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="2b8ed-113">Es gibt mehrere Möglichkeiten, eine CLSID zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="2b8ed-114">Im folgenden Beispiel wird das **DEFINE \_ GUID-Makro** verwendet:</span><span class="sxs-lookup"><span data-stu-id="2b8ed-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="2b8ed-115">Schreiben Sie als Nächstes eine Konstruktormethode für den Filter:</span><span class="sxs-lookup"><span data-stu-id="2b8ed-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="2b8ed-116">Beachten Sie, dass einer der Parameter für den [**CTransformFilter-Konstruktor**](ctransformfilter-ctransformfilter.md) die zuvor definierte CLSID ist.</span><span class="sxs-lookup"><span data-stu-id="2b8ed-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="2b8ed-117">Weiter: [Schritt 3. Unterstützung der Medientypaushandlung](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="2b8ed-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b8ed-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b8ed-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b8ed-119">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="2b8ed-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



