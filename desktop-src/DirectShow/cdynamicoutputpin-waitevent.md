---
description: Die waitevent-Methode wartet, bis das angegebene Ereignis signalisiert wird.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Cdynamicoutputpin. waitevent-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371656"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="c3507-103">Cdynamicoutputpin. waitevent-Methode</span><span class="sxs-lookup"><span data-stu-id="c3507-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="c3507-104">Die- `WaitEvent` Methode wartet, bis das angegebene Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3507-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3507-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3507-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c3507-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3507-107">*hevent*</span><span class="sxs-lookup"><span data-stu-id="c3507-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="c3507-108">Handle für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3507-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3507-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3507-109">Return value</span></span>

<span data-ttu-id="c3507-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c3507-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c3507-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3507-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c3507-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c3507-112">Return code</span></span>                                                                                  | <span data-ttu-id="c3507-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3507-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="c3507-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3507-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c3507-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c3507-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="c3507-116"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="c3507-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c3507-117">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c3507-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c3507-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3507-118">Requirements</span></span>



| <span data-ttu-id="c3507-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3507-119">Requirement</span></span> | <span data-ttu-id="c3507-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3507-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3507-121">Header</span><span class="sxs-lookup"><span data-stu-id="c3507-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c3507-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3507-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c3507-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3507-123">Library</span></span><br/> | <dl> <span data-ttu-id="c3507-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c3507-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3507-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3507-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3507-126">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c3507-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




