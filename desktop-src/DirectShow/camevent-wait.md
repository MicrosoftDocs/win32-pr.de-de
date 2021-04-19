---
description: Die Wait-Methode blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Camevent. Wait-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365732"
---
# <a name="cameventwait-method"></a><span data-ttu-id="0c43e-103">Camevent. Wait-Methode</span><span class="sxs-lookup"><span data-stu-id="0c43e-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="0c43e-104">Die- `Wait` Methode wird blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="0c43e-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c43e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c43e-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="0c43e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c43e-107">*dwtimeout*</span><span class="sxs-lookup"><span data-stu-id="0c43e-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="0c43e-108">Optionaler Timeout Wert, dargestellt in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="0c43e-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c43e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c43e-109">Return value</span></span>

<span data-ttu-id="0c43e-110">Gibt " **true** " zurück, wenn das Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c43e-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="0c43e-111">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c43e-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c43e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c43e-112">Remarks</span></span>

<span data-ttu-id="0c43e-113">Bei automatischen Zurücksetzungs Ereignissen wird das Ereignis auf einen nicht signalisierten Zustand zurückgesetzt, wenn diese Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c43e-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c43e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c43e-114">Requirements</span></span>



| <span data-ttu-id="0c43e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c43e-115">Requirement</span></span> | <span data-ttu-id="0c43e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0c43e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c43e-117">Header</span><span class="sxs-lookup"><span data-stu-id="0c43e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0c43e-118"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c43e-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0c43e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c43e-119">Library</span></span><br/> | <dl> <span data-ttu-id="0c43e-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0c43e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c43e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c43e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c43e-122">**Camevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0c43e-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




