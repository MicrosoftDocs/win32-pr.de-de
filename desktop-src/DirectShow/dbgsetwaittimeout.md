---
description: Legt den Timeout Wert für das Debuggen fest. Wird in Einzelhandels Builds ignoriert.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Dbgsetwaittimeout-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359307"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="66846-104">Dbgsetwaittimeout-Funktion</span><span class="sxs-lookup"><span data-stu-id="66846-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="66846-105">Legt den Timeout Wert für das Debuggen fest.</span><span class="sxs-lookup"><span data-stu-id="66846-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="66846-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66846-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="66846-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66846-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="66846-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66846-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66846-109">*dwtimeout*</span><span class="sxs-lookup"><span data-stu-id="66846-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="66846-110">Timeout Wert in Millisekunden oder unendlich, wenn unbegrenzt gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="66846-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66846-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66846-111">Return value</span></span>

<span data-ttu-id="66846-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="66846-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66846-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66846-113">Remarks</span></span>

<span data-ttu-id="66846-114">In Debugbuilds verwenden die Funktionen [**dbgwaitformultipleobjects**](dbgwaitformultipleobjects.md) und [**dbgwaitforsingleobject**](dbgwaitforsingleobject.md) diesen Wert als Timeout Intervall.</span><span class="sxs-lookup"><span data-stu-id="66846-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="66846-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66846-115">Requirements</span></span>



| <span data-ttu-id="66846-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66846-116">Requirement</span></span> | <span data-ttu-id="66846-117">Wert</span><span class="sxs-lookup"><span data-stu-id="66846-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66846-118">Header</span><span class="sxs-lookup"><span data-stu-id="66846-118">Header</span></span><br/>  | <dl> <span data-ttu-id="66846-119"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66846-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66846-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66846-120">Library</span></span><br/> | <dl> <span data-ttu-id="66846-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="66846-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66846-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66846-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66846-123">Wait-Debugging-Funktionen</span><span class="sxs-lookup"><span data-stu-id="66846-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




