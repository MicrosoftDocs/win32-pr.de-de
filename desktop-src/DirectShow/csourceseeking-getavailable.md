---
description: 'Die getavailable-Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist. Diese Methode implementiert die imediaseeking:: getavailable-Methode.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Csourceseeking. getavailable-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359407"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="09fea-104">Csourceseeking. getavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="09fea-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="09fea-105">Die- `GetAvailable` Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist.</span><span class="sxs-lookup"><span data-stu-id="09fea-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="09fea-106">Diese Methode implementiert die [**imediaseeking:: getavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) -Methode.</span><span class="sxs-lookup"><span data-stu-id="09fea-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09fea-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="09fea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09fea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fea-109">*pearliest*</span><span class="sxs-lookup"><span data-stu-id="09fea-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="09fea-110">Ein Zeiger auf eine Variable, die die früheste Zeit für eine effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="09fea-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="09fea-111">Die-Variable ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09fea-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="09fea-112">*platest*</span><span class="sxs-lookup"><span data-stu-id="09fea-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="09fea-113">Ein Zeiger auf eine Variable, die den letzten Zeitpunkt für die effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="09fea-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="09fea-114">Die-Variable wird auf den Wert der [**csourceseeking:: m \_ rtduration**](csourceseeking-m-rtduration.md) -Element Variablen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09fea-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fea-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09fea-115">Return value</span></span>

<span data-ttu-id="09fea-116">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="09fea-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fea-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09fea-117">Requirements</span></span>



| <span data-ttu-id="09fea-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09fea-118">Requirement</span></span> | <span data-ttu-id="09fea-119">Wert</span><span class="sxs-lookup"><span data-stu-id="09fea-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09fea-120">Header</span><span class="sxs-lookup"><span data-stu-id="09fea-120">Header</span></span><br/>  | <dl> <span data-ttu-id="09fea-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09fea-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09fea-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09fea-122">Library</span></span><br/> | <dl> <span data-ttu-id="09fea-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="09fea-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fea-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09fea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fea-125">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="09fea-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




