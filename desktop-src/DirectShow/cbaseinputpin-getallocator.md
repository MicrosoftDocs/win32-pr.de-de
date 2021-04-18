---
description: 'Die getallocator-Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin:: getallocator-Methode.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Cbasinput PIN. getallocator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368336"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="9ddbd-104">Cbasinput PIN. getallocator-Methode</span><span class="sxs-lookup"><span data-stu-id="9ddbd-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="9ddbd-105">Die- `GetAllocator` Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="9ddbd-106">Diese Methode implementiert die [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddbd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ddbd-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="9ddbd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ddbd-109">*ppzuzuweisung*</span><span class="sxs-lookup"><span data-stu-id="9ddbd-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="9ddbd-110">Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ddbd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ddbd-111">Return value</span></span>

<span data-ttu-id="9ddbd-112">Gibt " \_ OK" zurück, wenn erfolgreich, oder einen Fehlercode aus der **cokreateinzustance** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ddbd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ddbd-113">Remarks</span></span>

<span data-ttu-id="9ddbd-114">Diese Methode erstellt ein [**cmemzuordcator**](cmemallocator.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="9ddbd-115">Überschreiben Sie diese Methode, wenn der Filter eine Zuweisung aus einer downstreampin oder eine benutzerdefinierte Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="9ddbd-116">Wenn die Methode erfolgreich ausgeführt wird, hat die **imemzuordcator** -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="9ddbd-117">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="9ddbd-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ddbd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ddbd-118">Requirements</span></span>



| <span data-ttu-id="9ddbd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ddbd-119">Requirement</span></span> | <span data-ttu-id="9ddbd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9ddbd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddbd-121">Header</span><span class="sxs-lookup"><span data-stu-id="9ddbd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9ddbd-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ddbd-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ddbd-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ddbd-123">Library</span></span><br/> | <dl> <span data-ttu-id="9ddbd-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9ddbd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ddbd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ddbd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ddbd-126">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




