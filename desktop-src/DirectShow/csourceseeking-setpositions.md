---
description: 'Die setpositions-Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die imediaseeking:: setpositions-Methode.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Csourceseeking. setpositions-Methode (ctlutil. h)
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357691"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="05dc8-104">Csourceseeking. setpositions-Methode</span><span class="sxs-lookup"><span data-stu-id="05dc8-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="05dc8-105">Die `SetPositions` -Methode legt die aktuelle Position und die Position des Stopps fest.</span><span class="sxs-lookup"><span data-stu-id="05dc8-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="05dc8-106">Diese Methode implementiert die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode.</span><span class="sxs-lookup"><span data-stu-id="05dc8-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05dc8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05dc8-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="05dc8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05dc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05dc8-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="05dc8-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="05dc8-110">Ein Zeiger auf eine Variable, die die aktuelle Position angibt.</span><span class="sxs-lookup"><span data-stu-id="05dc8-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="05dc8-111">*Currentflags*</span><span class="sxs-lookup"><span data-stu-id="05dc8-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="05dc8-112">Bitweise Kombination von-Flags.</span><span class="sxs-lookup"><span data-stu-id="05dc8-112">Bitwise combination of flags.</span></span> <span data-ttu-id="05dc8-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="05dc8-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="05dc8-114">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="05dc8-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="05dc8-115">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats angibt.</span><span class="sxs-lookup"><span data-stu-id="05dc8-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="05dc8-116">*Stopflags*</span><span class="sxs-lookup"><span data-stu-id="05dc8-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="05dc8-117">Bitweise Kombination von-Flags.</span><span class="sxs-lookup"><span data-stu-id="05dc8-117">Bitwise combination of flags.</span></span> <span data-ttu-id="05dc8-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="05dc8-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05dc8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05dc8-119">Return value</span></span>

<span data-ttu-id="05dc8-120">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="05dc8-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="05dc8-121">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="05dc8-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="05dc8-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="05dc8-122">Return code</span></span>                                                                                  | <span data-ttu-id="05dc8-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05dc8-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="05dc8-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05dc8-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="05dc8-125">Erfolg</span><span class="sxs-lookup"><span data-stu-id="05dc8-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="05dc8-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="05dc8-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="05dc8-127">Ungültige Flags.</span><span class="sxs-lookup"><span data-stu-id="05dc8-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="05dc8-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="05dc8-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="05dc8-129">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="05dc8-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="05dc8-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05dc8-130">Remarks</span></span>

<span data-ttu-id="05dc8-131">Die folgenden Flags werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="05dc8-131">The following flags are supported:</span></span>

-   <span data-ttu-id="05dc8-132">\_Suchen von \_ noposior</span><span class="sxs-lookup"><span data-stu-id="05dc8-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="05dc8-133">\_Sucht nach \_ absolutepositionierung</span><span class="sxs-lookup"><span data-stu-id="05dc8-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="05dc8-134">\_Suche nach \_ relativepositionierung</span><span class="sxs-lookup"><span data-stu-id="05dc8-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="05dc8-135">\_ \_ Inkrementalpositionierung suchen (nur *Pend* )</span><span class="sxs-lookup"><span data-stu-id="05dc8-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="05dc8-136">Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="05dc8-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="05dc8-137">Diese Methode aktualisiert die Werte der [**csourceseeking:: m \_ rtstart**](csourceseeking-m-rtstart.md) -und [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) -Element Variablen und ruft dann die reinen virtuellen Methoden [**csourceseeking:: changestart**](csourceseeking-changestart.md) und [**csourceseeking:: changestoppt**](csourceseeking-changestop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="05dc8-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05dc8-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05dc8-138">Requirements</span></span>



| <span data-ttu-id="05dc8-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05dc8-139">Requirement</span></span> | <span data-ttu-id="05dc8-140">Wert</span><span class="sxs-lookup"><span data-stu-id="05dc8-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05dc8-141">Header</span><span class="sxs-lookup"><span data-stu-id="05dc8-141">Header</span></span><br/>  | <dl> <span data-ttu-id="05dc8-142"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05dc8-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05dc8-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05dc8-143">Library</span></span><br/> | <dl> <span data-ttu-id="05dc8-144">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="05dc8-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05dc8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05dc8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05dc8-146">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="05dc8-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




