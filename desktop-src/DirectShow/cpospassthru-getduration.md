---
description: 'Die getduration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die imediaseeking:: getduration-Methode.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Cpospassthru. getduration-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361275"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="4c06f-104">Cpospassthru. getduration-Methode</span><span class="sxs-lookup"><span data-stu-id="4c06f-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="4c06f-105">Die- `GetDuration` Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="4c06f-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="4c06f-106">Diese Methode implementiert die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4c06f-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c06f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c06f-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="4c06f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c06f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c06f-109">*pduration*</span><span class="sxs-lookup"><span data-stu-id="4c06f-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="4c06f-110">Ein Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="4c06f-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c06f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c06f-111">Return value</span></span>

<span data-ttu-id="4c06f-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="4c06f-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c06f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c06f-113">Requirements</span></span>



| <span data-ttu-id="4c06f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c06f-114">Requirement</span></span> | <span data-ttu-id="4c06f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4c06f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c06f-116">Header</span><span class="sxs-lookup"><span data-stu-id="4c06f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4c06f-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c06f-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4c06f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c06f-118">Library</span></span><br/> | <dl> <span data-ttu-id="4c06f-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4c06f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c06f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c06f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c06f-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4c06f-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




