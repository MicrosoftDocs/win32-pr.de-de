---
description: 'Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode implementiert die imemzuzucator:: SetProperties-Methode.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Cbasezucator. SetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359743"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="e850a-104">Cbasezucator. SetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="e850a-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="e850a-105">Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="e850a-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="e850a-106">Diese Methode implementiert die [**imemzuzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e850a-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e850a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e850a-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="e850a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e850a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e850a-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="e850a-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="e850a-110">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e850a-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="e850a-111">*pactual*</span><span class="sxs-lookup"><span data-stu-id="e850a-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="e850a-112">Ein Zeiger auf eine **\_ zuordnereigenschafts** -Struktur, die die tatsächlichen Puffer Eigenschaften empfängt.</span><span class="sxs-lookup"><span data-stu-id="e850a-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e850a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e850a-113">Return value</span></span>

<span data-ttu-id="e850a-114">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e850a-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="e850a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e850a-115">Return code</span></span>                                                                                                 | <span data-ttu-id="e850a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e850a-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="e850a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="e850a-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e850a-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="e850a-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="e850a-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e850a-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e850a-121"><dt>**VFW \_ E \_ \_ hat bereits ein Commit ausgeführt**</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="e850a-122">Der zugewiesene Arbeitsspeicher kann nicht geändert werden, solange der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e850a-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="e850a-123"><dt>**VFW \_ E \_ badalign**</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="e850a-124">Es wurde eine ungültige Ausrichtung angegeben.</span><span class="sxs-lookup"><span data-stu-id="e850a-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="e850a-125"><dt>**ausstehende VFW \_ E- \_ Puffer \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="e850a-126">Mindestens ein Puffer ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="e850a-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="e850a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e850a-127">Remarks</span></span>

<span data-ttu-id="e850a-128">Diese Methode gibt die Puffer Anforderungen an, weist jedoch keine Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="e850a-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="e850a-129">Nennen Sie die [**cbaseallocator:: Commit**](cbaseallocator-commit.md) -Methode, um Puffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e850a-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="e850a-130">Der Aufrufer ordnet zwei \_ zuordnereigenschafts-Strukturen zu.</span><span class="sxs-lookup"><span data-stu-id="e850a-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="e850a-131">Der *pRequest* -Parameter enthält die Puffer Anforderungen des Aufrufers, einschließlich der Anzahl der Puffer und der Größe der einzelnen Puffer.</span><span class="sxs-lookup"><span data-stu-id="e850a-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="e850a-132">Wenn die Methode zurückgibt, enthält der *pactual* -Parameter die tatsächlichen Puffer Eigenschaften, wie von der Zuweisung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e850a-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="e850a-133">In der Basisklasse entsprechen die tatsächlichen Eigenschaften immer den angeforderten Eigenschaften, wenn Sie davon ausgehen, dass die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e850a-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="e850a-134">Abgeleitete Klassen können dieses Verhalten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="e850a-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="e850a-135">Für die Zuweisung darf kein Commit ausgeführt werden, und es dürfen keine ausstehenden Puffer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e850a-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="e850a-136">In der Basisklasse muss die Ausrichtung gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="e850a-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="e850a-137">Die [**cmemzuordcator**](cmemallocator.md) -Klasse überschreibt diese Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e850a-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="e850a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e850a-138">Requirements</span></span>



| <span data-ttu-id="e850a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e850a-139">Requirement</span></span> | <span data-ttu-id="e850a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e850a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e850a-141">Header</span><span class="sxs-lookup"><span data-stu-id="e850a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="e850a-142"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e850a-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e850a-143">Library</span></span><br/> | <dl> <span data-ttu-id="e850a-144">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e850a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e850a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e850a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e850a-146">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e850a-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




