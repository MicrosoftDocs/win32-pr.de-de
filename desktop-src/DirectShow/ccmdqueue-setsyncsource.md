---
description: Mit der setsyncsource-Methode wird die Uhrzeit für die zeitliche Steuerung festgelegt.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Ccmdqueue. setsyncsource-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370499"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="169dc-103">Ccmdqueue. setsyncsource-Methode</span><span class="sxs-lookup"><span data-stu-id="169dc-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="169dc-104">Die- `SetSyncSource` Methode legt die Zeit für die zeitliche Steuerung fest.</span><span class="sxs-lookup"><span data-stu-id="169dc-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="169dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="169dc-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="169dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="169dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="169dc-107">*Pirc*</span><span class="sxs-lookup"><span data-stu-id="169dc-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="169dc-108">Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="169dc-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="169dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="169dc-109">Return value</span></span>

<span data-ttu-id="169dc-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="169dc-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="169dc-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="169dc-111">Requirements</span></span>



| <span data-ttu-id="169dc-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="169dc-112">Requirement</span></span> | <span data-ttu-id="169dc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="169dc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="169dc-114">Header</span><span class="sxs-lookup"><span data-stu-id="169dc-114">Header</span></span><br/>  | <dl> <span data-ttu-id="169dc-115"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="169dc-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="169dc-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="169dc-116">Library</span></span><br/> | <dl> <span data-ttu-id="169dc-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="169dc-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="169dc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="169dc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="169dc-119">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="169dc-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




