---
description: Die Copy-Methode kopiert ein Medien Beispiel.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Ctransinplacefilter. Copy-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370827"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="a77da-103">Ctransinplacefilter. Copy-Methode</span><span class="sxs-lookup"><span data-stu-id="a77da-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="a77da-104">Die- `Copy` Methode kopiert ein Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a77da-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77da-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="a77da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77da-107">*psource*</span><span class="sxs-lookup"><span data-stu-id="a77da-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="a77da-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="a77da-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77da-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a77da-109">Return value</span></span>

<span data-ttu-id="a77da-110">Gibt einen Zeiger auf die **imediasample** -Schnittstelle im neuen Beispiel zurück.</span><span class="sxs-lookup"><span data-stu-id="a77da-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77da-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a77da-111">Remarks</span></span>

<span data-ttu-id="a77da-112">Diese Methode ruft einen leeren Puffer von der Downstream-Zuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="a77da-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="a77da-113">Alle Beispiel Eigenschaften werden zusammen mit den eigentlichen Daten aus dem Beispiel aus *psource* in das neue Beispiel kopiert.</span><span class="sxs-lookup"><span data-stu-id="a77da-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="a77da-114">Wenn der Filter zwei Zuweisungen verwendet, wird diese Methode aufgerufen, um Daten über Puffer hinweg zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a77da-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77da-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a77da-115">Requirements</span></span>



| <span data-ttu-id="a77da-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a77da-116">Requirement</span></span> | <span data-ttu-id="a77da-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a77da-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77da-118">Header</span><span class="sxs-lookup"><span data-stu-id="a77da-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a77da-119"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a77da-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a77da-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a77da-120">Library</span></span><br/> | <dl> <span data-ttu-id="a77da-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a77da-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a77da-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a77da-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77da-123">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a77da-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




