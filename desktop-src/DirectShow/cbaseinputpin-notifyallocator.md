---
description: 'Die notifyzucator-Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die IMemInputPin:: notifyzucator-Methode implementiert.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Cbaseingeputpin. notifyzucator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355996"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="dc336-104">Cbaseingeputpin. notifyzucator-Methode</span><span class="sxs-lookup"><span data-stu-id="dc336-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="dc336-105">Die- `NotifyAllocator` Methode gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="dc336-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="dc336-106">Mit dieser Methode wird die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode implementiert.</span><span class="sxs-lookup"><span data-stu-id="dc336-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc336-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc336-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="dc336-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc336-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc336-109">*pallocator*</span><span class="sxs-lookup"><span data-stu-id="dc336-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="dc336-110">Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="dc336-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dc336-111">*nur Bread*</span><span class="sxs-lookup"><span data-stu-id="dc336-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="dc336-112">Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="dc336-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="dc336-113">**True** gibt an, dass die Beispiele schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="dc336-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc336-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc336-114">Return value</span></span>

<span data-ttu-id="dc336-115">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dc336-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc336-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc336-116">Remarks</span></span>

<span data-ttu-id="dc336-117">Während der Pin-Verbindung wählt die Ausgabe-PIN eine Zuweisung aus und ruft diese Methode auf, um die Eingabe-PIN zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="dc336-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="dc336-118">Die Ausgabepin kann die Zuweisung verwenden, die die Eingabe-PIN in der [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode vorgeschlagen hat, oder Sie kann Ihre eigene Zuweisung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dc336-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc336-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc336-119">Requirements</span></span>



| <span data-ttu-id="dc336-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc336-120">Requirement</span></span> | <span data-ttu-id="dc336-121">Wert</span><span class="sxs-lookup"><span data-stu-id="dc336-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc336-122">Header</span><span class="sxs-lookup"><span data-stu-id="dc336-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dc336-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc336-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dc336-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc336-124">Library</span></span><br/> | <dl> <span data-ttu-id="dc336-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dc336-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc336-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc336-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc336-127">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dc336-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




