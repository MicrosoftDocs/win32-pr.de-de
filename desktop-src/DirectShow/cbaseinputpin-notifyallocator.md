---
description: 'CBaseInputPin.NotifyAllocator-Methode: Die NotifyAllocator-Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die IMemInputPin::NotifyAllocator-Methode.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: CBaseInputPin.NotifyAllocator-Methode (Amfilter.h)
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
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099715"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="ebec5-104">CBaseInputPin.NotifyAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="ebec5-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="ebec5-105">Die `NotifyAllocator` -Methode gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="ebec5-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="ebec5-106">Diese Methode implementiert die [**IMemInputPin::NotifyAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="ebec5-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebec5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebec5-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="ebec5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebec5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebec5-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="ebec5-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="ebec5-110">Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="ebec5-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ebec5-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="ebec5-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="ebec5-112">Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="ebec5-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="ebec5-113">True gibt an, dass Beispiele schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="ebec5-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebec5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebec5-114">Return value</span></span>

<span data-ttu-id="ebec5-115">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ebec5-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebec5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebec5-116">Remarks</span></span>

<span data-ttu-id="ebec5-117">Während der Stecknadelverbindung wählt der Ausgabepin eine Zuweisung aus und ruft diese Methode auf, um den Eingabepin zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="ebec5-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="ebec5-118">Der Ausgabepin kann die Zuweisung verwenden, die der Eingabepin in der [**IMemInputPin::GetAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) vorgeschlagen hat, oder er kann einen eigenen Allocator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ebec5-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebec5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebec5-119">Requirements</span></span>



| <span data-ttu-id="ebec5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebec5-120">Requirement</span></span> | <span data-ttu-id="ebec5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ebec5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebec5-122">Header</span><span class="sxs-lookup"><span data-stu-id="ebec5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ebec5-123"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="ebec5-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ebec5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ebec5-124">Library</span></span><br/> | <dl> <span data-ttu-id="ebec5-125"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ebec5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebec5-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ebec5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebec5-127">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ebec5-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




