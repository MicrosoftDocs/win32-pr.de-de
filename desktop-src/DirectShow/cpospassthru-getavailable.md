---
description: 'Die getavailable-Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist. Diese Methode implementiert die imediaseeking:: getavailable-Methode.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Cpospassthru. getavailable-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360414"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="2d867-104">Cpospassthru. getavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="2d867-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="2d867-105">Die- `GetAvailable` Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist.</span><span class="sxs-lookup"><span data-stu-id="2d867-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="2d867-106">Diese Methode implementiert die [**imediaseeking:: getavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2d867-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d867-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d867-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="2d867-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d867-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d867-109">*pearliest*</span><span class="sxs-lookup"><span data-stu-id="2d867-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="2d867-110">Ein Zeiger auf eine Variable, die die früheste Zeit für eine effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d867-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="2d867-111">*platest*</span><span class="sxs-lookup"><span data-stu-id="2d867-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="2d867-112">Ein Zeiger auf eine Variable, die den letzten Zeitpunkt für die effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d867-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d867-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d867-113">Return value</span></span>

<span data-ttu-id="2d867-114">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="2d867-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d867-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d867-115">Requirements</span></span>



| <span data-ttu-id="2d867-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d867-116">Requirement</span></span> | <span data-ttu-id="2d867-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2d867-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d867-118">Header</span><span class="sxs-lookup"><span data-stu-id="2d867-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2d867-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d867-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d867-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d867-120">Library</span></span><br/> | <dl> <span data-ttu-id="2d867-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d867-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d867-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d867-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d867-123">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2d867-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




