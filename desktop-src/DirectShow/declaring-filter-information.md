---
description: Deklarieren von Filter Informationen
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Deklarieren von Filter Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747409"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="27f74-103">Deklarieren von Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="27f74-103">Declaring Filter Information</span></span>

<span data-ttu-id="27f74-104">Der erste Schritt besteht darin, die Filter Informationen bei Bedarf zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="27f74-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="27f74-105">DirectShow definiert die folgenden Strukturen zum Beschreiben von Filtern, Pins und Medientypen:</span><span class="sxs-lookup"><span data-stu-id="27f74-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="27f74-106">Struktur</span><span class="sxs-lookup"><span data-stu-id="27f74-106">Structure</span></span>                                               | <span data-ttu-id="27f74-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27f74-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="27f74-108">**amoviesetup- \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="27f74-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="27f74-109">Beschreibt einen Filter.</span><span class="sxs-lookup"><span data-stu-id="27f74-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="27f74-110">**amoviesetup- \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="27f74-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="27f74-111">Beschreibt eine PIN.</span><span class="sxs-lookup"><span data-stu-id="27f74-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="27f74-112">**amoviesetup- \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="27f74-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="27f74-113">Beschreibt einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="27f74-113">Describes a media type.</span></span> |



 

<span data-ttu-id="27f74-114">Diese Strukturen sind eingebettet.</span><span class="sxs-lookup"><span data-stu-id="27f74-114">These structures are nested.</span></span> <span data-ttu-id="27f74-115">Die **amoveiesetup- \_ Filter** Struktur verfügt über einen Zeiger auf ein Array von **amoviesetup- \_ Pin** -Strukturen, die jeweils über einen Zeiger auf ein Array von **amoveiesetup \_ mediaType** -Strukturen verfügen.</span><span class="sxs-lookup"><span data-stu-id="27f74-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="27f74-116">Zusammenstellen diese Strukturen ausreichend Informationen für die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle bereit, um einen Filter zu suchen.</span><span class="sxs-lookup"><span data-stu-id="27f74-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="27f74-117">Dabei handelt es sich nicht um eine komplette Beschreibung eines Filters.</span><span class="sxs-lookup"><span data-stu-id="27f74-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="27f74-118">Wenn der Filter beispielsweise mehrere Instanzen derselben Pin erstellt, sollten Sie nur eine [**amoviesetup- \_ Pin**](amoviesetup-pin.md) -Struktur für diese Pin deklarieren.</span><span class="sxs-lookup"><span data-stu-id="27f74-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="27f74-119">Außerdem ist kein Filter erforderlich, um jede Kombination von Medientypen zu unterstützen, die registriert werden. Es ist auch nicht erforderlich, jeden Medientyp zu registrieren, den er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27f74-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="27f74-120">Deklarieren Sie die Setup Strukturen als globale Variablen in der dll.</span><span class="sxs-lookup"><span data-stu-id="27f74-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="27f74-121">Das folgende Beispiel zeigt einen Filter mit einer Ausgabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="27f74-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="27f74-122">Der Filter Name wird als statische globale Variable deklariert, da er an anderer Stelle wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27f74-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27f74-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27f74-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f74-124">Registrieren von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="27f74-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



