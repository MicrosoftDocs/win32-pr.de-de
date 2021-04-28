---
description: 'CSourceSeeking.SetRate-Methode: Die SetRate-Methode legt die Wiedergaberate fest. Diese Methode implementiert die IMediaSeeking::SetRate-Methode.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: CSourceSeeking.SetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098738"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="4e76b-104">CSourceSeeking.SetRate-Methode</span><span class="sxs-lookup"><span data-stu-id="4e76b-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="4e76b-105">Die `SetRate` -Methode legt die Wiedergaberate fest.</span><span class="sxs-lookup"><span data-stu-id="4e76b-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="4e76b-106">Diese Methode implementiert die [**IMediaSeeking::SetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="4e76b-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e76b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e76b-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="4e76b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e76b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e76b-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="4e76b-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="4e76b-110">Wiedergaberate.</span><span class="sxs-lookup"><span data-stu-id="4e76b-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e76b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e76b-111">Return value</span></span>

<span data-ttu-id="4e76b-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e76b-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e76b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e76b-113">Remarks</span></span>

<span data-ttu-id="4e76b-114">Diese Methode aktualisiert den Wert der [**CSourceSeeking::m \_ dRateSeeking-Membervariablen**](csourceseeking-m-drateseeking.md) und ruft dann die reine virtuelle Methode [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)auf.</span><span class="sxs-lookup"><span data-stu-id="4e76b-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="4e76b-115">Die -Methode überprüft den *dRate-Parameter* nicht.</span><span class="sxs-lookup"><span data-stu-id="4e76b-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e76b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e76b-116">Requirements</span></span>



| <span data-ttu-id="4e76b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e76b-117">Requirement</span></span> | <span data-ttu-id="4e76b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4e76b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e76b-119">Header</span><span class="sxs-lookup"><span data-stu-id="4e76b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4e76b-120"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e76b-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e76b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e76b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4e76b-122"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4e76b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e76b-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e76b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e76b-124">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4e76b-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




