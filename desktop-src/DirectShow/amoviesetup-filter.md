---
description: Die amoviesetup- \_ Filter Struktur enthält Informationen zum Registrieren eines Filters.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER-Struktur (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361656"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="23fb9-103">Amoviesetup- \_ Filter Struktur</span><span class="sxs-lookup"><span data-stu-id="23fb9-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="23fb9-104">Die **amoviesetup- \_ Filter** Struktur enthält Informationen zum Registrieren eines Filters.</span><span class="sxs-lookup"><span data-stu-id="23fb9-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23fb9-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="23fb9-106">Member</span><span class="sxs-lookup"><span data-stu-id="23fb9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="23fb9-107">**clsID**</span><span class="sxs-lookup"><span data-stu-id="23fb9-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="23fb9-108">Klassen Bezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="23fb9-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="23fb9-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="23fb9-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="23fb9-110">Name des Filters.</span><span class="sxs-lookup"><span data-stu-id="23fb9-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="23fb9-111">**dwmerit**</span><span class="sxs-lookup"><span data-stu-id="23fb9-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="23fb9-112">Filter Verdienst.</span><span class="sxs-lookup"><span data-stu-id="23fb9-112">Filter merit.</span></span> <span data-ttu-id="23fb9-113">Wird von der [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle beim Erstellen eines Filter Diagramms verwendet.</span><span class="sxs-lookup"><span data-stu-id="23fb9-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="23fb9-114">Eine Liste der Verdienst Werte finden Sie unter [Verdienst](merit.md).</span><span class="sxs-lookup"><span data-stu-id="23fb9-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="23fb9-115">**npins**</span><span class="sxs-lookup"><span data-stu-id="23fb9-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="23fb9-116">Anzahl der Elemente im *lppin* -Array.</span><span class="sxs-lookup"><span data-stu-id="23fb9-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="23fb9-117">Wenn *lppin* **null** ist, legen Sie diesen Member auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="23fb9-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="23fb9-118">**lppin**</span><span class="sxs-lookup"><span data-stu-id="23fb9-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="23fb9-119">Zeiger auf ein Array von [**amoviesetup- \_ Pin**](amoviesetup-pin.md) -Strukturen der Größe *npins*.</span><span class="sxs-lookup"><span data-stu-id="23fb9-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="23fb9-120">Jedes Element dieses Arrays beschreibt eine PIN für den Filter.</span><span class="sxs-lookup"><span data-stu-id="23fb9-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23fb9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23fb9-121">Remarks</span></span>

<span data-ttu-id="23fb9-122">Weitere Informationen zur Verwendung dieser Struktur finden Sie unter [Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="23fb9-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="23fb9-123">Verwenden Sie diese Struktur nur für Filter, die in der Standardfilter Kategorie (CLSID \_ legacyamfiltercategory) registriert sind.</span><span class="sxs-lookup"><span data-stu-id="23fb9-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="23fb9-124">Um einen Filter in einer anderen Kategorie zu registrieren, verwenden Sie die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode, wie unter [Implementieren von DllRegisterServer](implementing-dllregisterserver.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23fb9-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="23fb9-125">Die Header Datei "ComBase. h" wird mit den [DirectShow-Basisklassen](directshow-base-classes.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="23fb9-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23fb9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23fb9-126">Requirements</span></span>



| <span data-ttu-id="23fb9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23fb9-127">Requirement</span></span> | <span data-ttu-id="23fb9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="23fb9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fb9-129">Header</span><span class="sxs-lookup"><span data-stu-id="23fb9-129">Header</span></span><br/> | <dl> <span data-ttu-id="23fb9-130"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23fb9-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23fb9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23fb9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fb9-132">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="23fb9-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




