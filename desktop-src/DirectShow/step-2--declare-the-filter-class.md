---
description: 'Schritt 2:'
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Schritt 2: Deklarieren der Filter Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369734"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="c0119-104">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="c0119-104">Step 2.</span></span> <span data-ttu-id="c0119-105">Deklarieren der Filter Klasse</span><span class="sxs-lookup"><span data-stu-id="c0119-105">Declare the Filter Class</span></span>

<span data-ttu-id="c0119-106">Dies ist Schritt 2 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c0119-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="c0119-107">Deklarieren Sie zunächst eine C++-Klasse, die die Basisklasse erbt:</span><span class="sxs-lookup"><span data-stu-id="c0119-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="c0119-108">Jeder der Filterklassen sind PIN-Klassen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0119-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="c0119-109">Abhängig von den spezifischen Anforderungen Ihres Filters müssen Sie möglicherweise die PIN-Klassen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c0119-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="c0119-110">Im Fall von **ctransformfilter** delegieren die Pins den größten Teil ihrer Arbeit an den Filter, sodass Sie die Pins wahrscheinlich nicht außer Kraft setzen müssen.</span><span class="sxs-lookup"><span data-stu-id="c0119-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="c0119-111">Sie müssen eine eindeutige CLSID für den Filter generieren.</span><span class="sxs-lookup"><span data-stu-id="c0119-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="c0119-112">Sie können das Hilfsprogramm GUIDGEN oder uuidgen verwenden. Kopieren Sie niemals eine vorhandene GUID.</span><span class="sxs-lookup"><span data-stu-id="c0119-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="c0119-113">Es gibt mehrere Möglichkeiten, eine CLSID zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c0119-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="c0119-114">Im folgenden Beispiel wird das **\_ GUID** -Makro definieren verwendet:</span><span class="sxs-lookup"><span data-stu-id="c0119-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="c0119-115">Schreiben Sie als nächstes eine Konstruktormethode für den Filter:</span><span class="sxs-lookup"><span data-stu-id="c0119-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="c0119-116">Beachten Sie, dass einer der Parameter für den [**ctransformfilter**](ctransformfilter-ctransformfilter.md) -Konstruktor die zuvor definierte CLSID ist.</span><span class="sxs-lookup"><span data-stu-id="c0119-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="c0119-117">Weiter: [Schritt 3. Unterstützung der Medientyp Aushandlung](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="c0119-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0119-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0119-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0119-119">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="c0119-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



