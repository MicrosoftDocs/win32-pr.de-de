---
description: Die checktime-Methode bestimmt, ob eine angegebene Zeit fällig ist.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Ccmdqueue. checktime-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372753"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="63989-103">Ccmdqueue. checktime-Methode</span><span class="sxs-lookup"><span data-stu-id="63989-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="63989-104">Die- `CheckTime` Methode bestimmt, ob eine angegebene Zeit fällig ist.</span><span class="sxs-lookup"><span data-stu-id="63989-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="63989-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63989-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="63989-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63989-107">*time*</span><span class="sxs-lookup"><span data-stu-id="63989-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="63989-108">Zeit bis zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="63989-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="63989-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="63989-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="63989-110">**True** , wenn der *Zeit* Parameter ein streamzeitwert ist. **False** , wenn *time* ein Präsentationszeit Wert ist.</span><span class="sxs-lookup"><span data-stu-id="63989-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63989-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63989-111">Return value</span></span>

<span data-ttu-id="63989-112">Gibt **true** zurück, wenn die angegebene Zeit noch nicht überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="63989-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="63989-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63989-113">Requirements</span></span>



| <span data-ttu-id="63989-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63989-114">Requirement</span></span> | <span data-ttu-id="63989-115">Wert</span><span class="sxs-lookup"><span data-stu-id="63989-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63989-116">Header</span><span class="sxs-lookup"><span data-stu-id="63989-116">Header</span></span><br/>  | <dl> <span data-ttu-id="63989-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63989-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63989-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63989-118">Library</span></span><br/> | <dl> <span data-ttu-id="63989-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="63989-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63989-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63989-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63989-121">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="63989-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




