---
description: 'Die Methode "Zuweisung" weist Speicher für die Puffer zu. Diese Methode überschreibt die cbasezucator:: Zuordnungsmethode.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Cimagezuzuordcator. Zuordnungsmethode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361564"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="4a01a-104">Cimagezuzuordcator. Zuordnungsmethode</span><span class="sxs-lookup"><span data-stu-id="4a01a-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="4a01a-105">Die- `Alloc` Methode weist Speicher für die Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="4a01a-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="4a01a-106">Diese Methode überschreibt die [**cbasezucator:: Zuordnungsmethode**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="4a01a-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a01a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a01a-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="4a01a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a01a-108">Parameters</span></span>

<span data-ttu-id="4a01a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4a01a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a01a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a01a-110">Return value</span></span>

<span data-ttu-id="4a01a-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4a01a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a01a-112">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="4a01a-112">Possible values include the following.</span></span>



| <span data-ttu-id="4a01a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4a01a-113">Return code</span></span>                                                                                   | <span data-ttu-id="4a01a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a01a-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="4a01a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a01a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4a01a-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="4a01a-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="4a01a-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4a01a-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4a01a-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="4a01a-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a01a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a01a-119">Remarks</span></span>

<span data-ttu-id="4a01a-120">Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen, wenn der Filter einen Commit für die Zuweisung ausführt.</span><span class="sxs-lookup"><span data-stu-id="4a01a-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="4a01a-121">Diese Methode erstellt eine Liste von Medien Beispielen, die als [**cimagesample**](cimagesample.md) -Objekte implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a01a-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="4a01a-122">Jedes Beispiel enthält eine GDI-geräteunabhängige Bitmap, die die GDI-Funktion " **foratedibsection** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a01a-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="4a01a-123">Intern ruft diese Methode [**cimagezuordcator:: kreatedib**](cimageallocator-createdib.md) auf, um jedes DIB zu erstellen, und [**cimagezuordcator:: forateimagesample**](cimageallocator-createimagesample.md) , um die einzelnen Beispiele zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a01a-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a01a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a01a-124">Requirements</span></span>



| <span data-ttu-id="4a01a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a01a-125">Requirement</span></span> | <span data-ttu-id="4a01a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4a01a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a01a-127">Header</span><span class="sxs-lookup"><span data-stu-id="4a01a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4a01a-128"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a01a-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a01a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a01a-129">Library</span></span><br/> | <dl> <span data-ttu-id="4a01a-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4a01a-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a01a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a01a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a01a-132">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4a01a-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




