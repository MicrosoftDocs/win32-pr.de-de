---
description: Mit der registermediatime-Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert. Diese Methode verwendet die Parameter " *StartTime* " und " *EndTime* ".
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: 'Crendererpospassthru. registermediatime-Methode (ctlutil. h): StartTime-und EndTime-Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372551"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="dc36c-104">Crendererpospassthru. registermediatime-Methode (ctlutil. h): StartTime-und EndTime-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc36c-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="dc36c-105">Mit der [**registermediatime**](crendererpospassthru-registermediatime.md) -Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc36c-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc36c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc36c-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="dc36c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc36c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc36c-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="dc36c-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="dc36c-109">Beispiel Startzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="dc36c-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="dc36c-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="dc36c-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="dc36c-111">Beispiel Endzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="dc36c-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc36c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc36c-112">Return value</span></span>

<span data-ttu-id="dc36c-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dc36c-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dc36c-114">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="dc36c-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="dc36c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dc36c-115">Return code</span></span>                                                                          | <span data-ttu-id="dc36c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc36c-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dc36c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc36c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc36c-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="dc36c-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc36c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc36c-119">Remarks</span></span>

<span data-ttu-id="dc36c-120">Diese Methode speichert die Zeitstempel Werte, die in " *StartTime* " und " *EndTime*" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dc36c-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="dc36c-121">Die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode ruft die gleichen Werte ab.</span><span class="sxs-lookup"><span data-stu-id="dc36c-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="dc36c-122">Der Filter sollte diese Methode für jedes empfangene Beispiel aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dc36c-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="dc36c-123">Die-Methode ist überladen, um entweder einen Zeiger auf das Beispiel oder den Zeitstempelwert selbst zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="dc36c-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc36c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc36c-124">Requirements</span></span>



| <span data-ttu-id="dc36c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc36c-125">Requirement</span></span> | <span data-ttu-id="dc36c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dc36c-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc36c-127">Header</span><span class="sxs-lookup"><span data-stu-id="dc36c-127">Header</span></span>  | <span data-ttu-id="dc36c-128">Ctlutil. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="dc36c-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="dc36c-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc36c-129">Library</span></span> | <span data-ttu-id="dc36c-130">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="dc36c-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




