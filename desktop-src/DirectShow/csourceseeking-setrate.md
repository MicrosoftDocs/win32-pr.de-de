---
description: 'Die setRate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaseeking:: Server trate-Methode.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Csourceseeking. ctrate-Methode (ctlutil. h)
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354190"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="0e612-104">Csourceseeking. ctrate-Methode</span><span class="sxs-lookup"><span data-stu-id="0e612-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="0e612-105">Die- `SetRate` Methode legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="0e612-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="0e612-106">Diese Methode implementiert die [**imediaseeking:: Server trate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0e612-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e612-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e612-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="0e612-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e612-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e612-109">*drate*</span><span class="sxs-lookup"><span data-stu-id="0e612-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="0e612-110">Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="0e612-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e612-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e612-111">Return value</span></span>

<span data-ttu-id="0e612-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0e612-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e612-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e612-113">Remarks</span></span>

<span data-ttu-id="0e612-114">Diese Methode aktualisiert den Wert der [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) -Element Variablen und ruft dann die rein virtuelle Methode [**csourceseeking:: changerate**](csourceseeking-changerate.md)auf.</span><span class="sxs-lookup"><span data-stu-id="0e612-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="0e612-115">Der *drate* -Parameter wird von der-Methode nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="0e612-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e612-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e612-116">Requirements</span></span>



| <span data-ttu-id="0e612-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e612-117">Requirement</span></span> | <span data-ttu-id="0e612-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0e612-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e612-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e612-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e612-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e612-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e612-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e612-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e612-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0e612-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e612-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e612-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e612-124">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0e612-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




