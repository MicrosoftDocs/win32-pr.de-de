---
description: Gibt false zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Critcheckout-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352947"
---
# <a name="critcheckout-function"></a><span data-ttu-id="dc7a5-103">Critcheckout-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc7a5-103">CritCheckOut function</span></span>

<span data-ttu-id="dc7a5-104">Gibt **false** zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc7a5-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="dc7a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc7a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7a5-107">*pccrit*</span><span class="sxs-lookup"><span data-stu-id="dc7a5-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="dc7a5-108">Zeiger auf einen kritischen [**ccritsec**](ccritsec.md) -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7a5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc7a5-109">Return value</span></span>

<span data-ttu-id="dc7a5-110">In Debugbuilds gibt **false** zurück, wenn der aktuelle Thread der Besitzer dieses kritischen Abschnitts ist, andernfalls **true** .</span><span class="sxs-lookup"><span data-stu-id="dc7a5-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="dc7a5-111">In Einzelhandels Builds gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc7a5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc7a5-112">Remarks</span></span>

<span data-ttu-id="dc7a5-113">Diese Funktion ist die Umkehrung der [**critcheckin**](critcheckin.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="dc7a5-114">Wenn **critcheckin** **true** zurückgibt, gibt **critcheckout** **false** zurück und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7a5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc7a5-115">Requirements</span></span>



| <span data-ttu-id="dc7a5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc7a5-116">Requirement</span></span> | <span data-ttu-id="dc7a5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dc7a5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7a5-118">Header</span><span class="sxs-lookup"><span data-stu-id="dc7a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dc7a5-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc7a5-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dc7a5-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc7a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="dc7a5-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="dc7a5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc7a5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc7a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7a5-123">Kritische Abschnitts Debuggingfunktionen</span><span class="sxs-lookup"><span data-stu-id="dc7a5-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




