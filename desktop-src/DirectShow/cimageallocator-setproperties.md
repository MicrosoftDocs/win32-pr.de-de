---
description: 'Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode überschreibt die cbasezucator:: SetProperties-Methode.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Cimagezuzuordcator. SetProperties-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372225"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="6f4f2-104">Cimagezuzuordcator. SetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="6f4f2-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="6f4f2-105">Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="6f4f2-106">Diese Methode überschreibt die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f4f2-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="6f4f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f4f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4f2-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="6f4f2-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="6f4f2-110">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="6f4f2-111">*pactual*</span><span class="sxs-lookup"><span data-stu-id="6f4f2-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="6f4f2-112">Ein Zeiger auf eine **\_ zuordnereigenschafts** -Struktur, die die tatsächlichen Puffer Eigenschaften empfängt.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f4f2-113">Return value</span></span>

<span data-ttu-id="6f4f2-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f4f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f4f2-115">Remarks</span></span>

<span data-ttu-id="6f4f2-116">Diese Methode ruft [**cimagezuordcator:: checksizes**](cimageallocator-checksizes.md) auf, um die angeforderte Puffergröße zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6f4f2-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="6f4f2-117">Außerdem wird die Basisklassen Version von aufgerufen `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="6f4f2-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4f2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f4f2-118">Requirements</span></span>



| <span data-ttu-id="6f4f2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f4f2-119">Requirement</span></span> | <span data-ttu-id="6f4f2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6f4f2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4f2-121">Header</span><span class="sxs-lookup"><span data-stu-id="6f4f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6f4f2-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f4f2-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6f4f2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f4f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="6f4f2-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6f4f2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4f2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f4f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4f2-126">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6f4f2-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




