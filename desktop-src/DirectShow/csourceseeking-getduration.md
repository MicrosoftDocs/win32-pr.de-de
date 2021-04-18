---
description: 'Die getduration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die imediaseeking:: getduration-Methode.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Csourceseeking. getduration-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354646"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="76887-104">Csourceseeking. getduration-Methode</span><span class="sxs-lookup"><span data-stu-id="76887-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="76887-105">Die- `GetDuration` Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="76887-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="76887-106">Diese Methode implementiert die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode.</span><span class="sxs-lookup"><span data-stu-id="76887-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76887-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76887-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="76887-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76887-109">*pduration*</span><span class="sxs-lookup"><span data-stu-id="76887-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="76887-110">Ein Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="76887-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76887-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76887-111">Return value</span></span>

<span data-ttu-id="76887-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="76887-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="76887-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76887-113">Return code</span></span>                                                                               | <span data-ttu-id="76887-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76887-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="76887-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76887-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="76887-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="76887-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="76887-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="76887-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="76887-118">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="76887-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76887-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76887-119">Remarks</span></span>

<span data-ttu-id="76887-120">Die Dauer wird von der [**csourceseeking:: m \_ rtduration**](csourceseeking-m-rtduration.md) -Element Variablen angegeben.</span><span class="sxs-lookup"><span data-stu-id="76887-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="76887-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76887-121">Requirements</span></span>



| <span data-ttu-id="76887-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76887-122">Requirement</span></span> | <span data-ttu-id="76887-123">Wert</span><span class="sxs-lookup"><span data-stu-id="76887-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76887-124">Header</span><span class="sxs-lookup"><span data-stu-id="76887-124">Header</span></span><br/>  | <dl> <span data-ttu-id="76887-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76887-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="76887-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76887-126">Library</span></span><br/> | <dl> <span data-ttu-id="76887-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="76887-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76887-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76887-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76887-129">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76887-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




