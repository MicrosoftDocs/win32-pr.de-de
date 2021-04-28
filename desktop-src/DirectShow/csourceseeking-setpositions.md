---
description: 'CSourceSeeking.SetPositions-Methode: Die SetPositions-Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die IMediaSeeking::SetPositions-Methode.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: CSourceSeeking.SetPositions-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085168"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="09d5f-104">CSourceSeeking.SetPositions-Methode</span><span class="sxs-lookup"><span data-stu-id="09d5f-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="09d5f-105">Die `SetPositions` -Methode legt die aktuelle Position und die Stoppposition fest.</span><span class="sxs-lookup"><span data-stu-id="09d5f-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="09d5f-106">Diese Methode implementiert die [**IMediaSeeking::SetPositions-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="09d5f-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d5f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09d5f-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="09d5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09d5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d5f-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="09d5f-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="09d5f-110">Zeiger auf eine Variable, die die aktuelle Position angibt.</span><span class="sxs-lookup"><span data-stu-id="09d5f-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="09d5f-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="09d5f-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="09d5f-112">Bitweise Kombination von Flags.</span><span class="sxs-lookup"><span data-stu-id="09d5f-112">Bitwise combination of flags.</span></span> <span data-ttu-id="09d5f-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09d5f-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="09d5f-114">*Pstop*</span><span class="sxs-lookup"><span data-stu-id="09d5f-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="09d5f-115">Zeiger auf eine Variable, die die Stoppzeit in Einheiten des aktuellen Zeitformats angibt.</span><span class="sxs-lookup"><span data-stu-id="09d5f-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="09d5f-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="09d5f-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="09d5f-117">Bitweise Kombination von Flags.</span><span class="sxs-lookup"><span data-stu-id="09d5f-117">Bitwise combination of flags.</span></span> <span data-ttu-id="09d5f-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09d5f-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d5f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09d5f-119">Return value</span></span>

<span data-ttu-id="09d5f-120">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="09d5f-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09d5f-121">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="09d5f-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="09d5f-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="09d5f-122">Return code</span></span>                                                                                  | <span data-ttu-id="09d5f-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09d5f-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="09d5f-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09d5f-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="09d5f-125">Erfolg</span><span class="sxs-lookup"><span data-stu-id="09d5f-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="09d5f-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="09d5f-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="09d5f-127">Ungültige Flags</span><span class="sxs-lookup"><span data-stu-id="09d5f-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="09d5f-128"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="09d5f-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="09d5f-129">**NULL-Zeigerargument**</span><span class="sxs-lookup"><span data-stu-id="09d5f-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09d5f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09d5f-130">Remarks</span></span>

<span data-ttu-id="09d5f-131">Die folgenden Flags werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="09d5f-131">The following flags are supported:</span></span>

-   <span data-ttu-id="09d5f-132">AM \_ SEEKING \_ NoPositioning</span><span class="sxs-lookup"><span data-stu-id="09d5f-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="09d5f-133">AM \_ SEEKING \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="09d5f-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="09d5f-134">AM \_ SEEKING \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="09d5f-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="09d5f-135">AM \_ SEEKING \_ IncrementalPositioning ( nur *pStop)*</span><span class="sxs-lookup"><span data-stu-id="09d5f-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="09d5f-136">Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="09d5f-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="09d5f-137">Diese Methode aktualisiert die Werte der Membervariablen [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) und [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) und ruft dann die reinen virtuellen Methoden [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) und [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="09d5f-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09d5f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09d5f-138">Requirements</span></span>



| <span data-ttu-id="09d5f-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09d5f-139">Requirement</span></span> | <span data-ttu-id="09d5f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="09d5f-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d5f-141">Header</span><span class="sxs-lookup"><span data-stu-id="09d5f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="09d5f-142"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="09d5f-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09d5f-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09d5f-143">Library</span></span><br/> | <dl> <span data-ttu-id="09d5f-144"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="09d5f-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d5f-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09d5f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d5f-146">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="09d5f-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




