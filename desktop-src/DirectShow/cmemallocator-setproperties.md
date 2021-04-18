---
description: Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Cmemzuzucator. SetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357708"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="eb5aa-103">Cmemzuzucator. SetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="eb5aa-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="eb5aa-104">Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb5aa-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="eb5aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb5aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb5aa-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="eb5aa-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="eb5aa-108">Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="eb5aa-109">*pactual*</span><span class="sxs-lookup"><span data-stu-id="eb5aa-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="eb5aa-110">Ein Zeiger auf eine **\_ zuordnereigenschafts** -Struktur, die die tatsächlichen Puffer Eigenschaften empfängt.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb5aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb5aa-111">Return value</span></span>

<span data-ttu-id="eb5aa-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="eb5aa-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eb5aa-113">Return code</span></span>                                                                                                 | <span data-ttu-id="eb5aa-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb5aa-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb5aa-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="eb5aa-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="eb5aa-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="eb5aa-118">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="eb5aa-119"><dt>**VFW \_ E \_ \_ hat bereits ein Commit ausgeführt**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="eb5aa-120">Der zugewiesene Arbeitsspeicher kann nicht geändert werden, solange der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="eb5aa-121"><dt>**VFW \_ E \_ badalign**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="eb5aa-122">Es wurde eine ungültige Ausrichtung angegeben.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="eb5aa-123"><dt>**ausstehende VFW \_ E- \_ Puffer \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="eb5aa-124">Mindestens ein Puffer ist noch aktiv.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="eb5aa-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb5aa-125">Remarks</span></span>

<span data-ttu-id="eb5aa-126">Diese Methode überschreibt die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="eb5aa-127">Die Puffer Ausrichtung, die vom **cbalign** -Member der **Zuweisungs \_ Eigenschafts** Struktur angegeben wird, muss eine selbst Potenz von zwei sein.</span><span class="sxs-lookup"><span data-stu-id="eb5aa-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb5aa-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb5aa-128">Requirements</span></span>



| <span data-ttu-id="eb5aa-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb5aa-129">Requirement</span></span> | <span data-ttu-id="eb5aa-130">Wert</span><span class="sxs-lookup"><span data-stu-id="eb5aa-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5aa-131">Header</span><span class="sxs-lookup"><span data-stu-id="eb5aa-131">Header</span></span><br/>  | <dl> <span data-ttu-id="eb5aa-132"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb5aa-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb5aa-133">Library</span></span><br/> | <dl> <span data-ttu-id="eb5aa-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb5aa-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb5aa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb5aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb5aa-136">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb5aa-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




