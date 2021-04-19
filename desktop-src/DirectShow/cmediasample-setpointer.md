---
description: Die setpointer-Methode legt den Zeiger auf den Arbeitsspeicher Puffer fest.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Cmediasample. setpointer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370572"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="28500-103">Cmediasample. setpointer-Methode</span><span class="sxs-lookup"><span data-stu-id="28500-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="28500-104">Die- `SetPointer` Methode legt den Zeiger auf den Arbeitsspeicher Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="28500-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="28500-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28500-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="28500-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28500-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="28500-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="28500-108">Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größe von *cbytes*.</span><span class="sxs-lookup"><span data-stu-id="28500-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="28500-109">*cbytes*</span><span class="sxs-lookup"><span data-stu-id="28500-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="28500-110">Länge des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="28500-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28500-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28500-111">Return value</span></span>

<span data-ttu-id="28500-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="28500-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="28500-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28500-113">Remarks</span></span>

<span data-ttu-id="28500-114">Diese Methode ermöglicht es der Zuweisung, einen neuen Zeiger für das Beispiel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="28500-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="28500-115">Diese Methode ist nicht über die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28500-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="28500-116">Das Objekt, das das Beispiel erstellt, kann auf diese Methode (über **cmediasample**) zugreifen, andere Objekte hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="28500-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="28500-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28500-117">Requirements</span></span>



| <span data-ttu-id="28500-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28500-118">Requirement</span></span> | <span data-ttu-id="28500-119">Wert</span><span class="sxs-lookup"><span data-stu-id="28500-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28500-120">Header</span><span class="sxs-lookup"><span data-stu-id="28500-120">Header</span></span><br/>  | <dl> <span data-ttu-id="28500-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28500-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="28500-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28500-122">Library</span></span><br/> | <dl> <span data-ttu-id="28500-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="28500-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28500-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28500-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28500-125">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="28500-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




