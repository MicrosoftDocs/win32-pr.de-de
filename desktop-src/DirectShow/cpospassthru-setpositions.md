---
description: 'CPosPassThru.SetPositions-Methode: Die SetPositions-Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die IMediaSeeking::SetPositions-Methode.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: CPosPassThru.SetPositions-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085478"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="89911-104">CPosPassThru.SetPositions-Methode</span><span class="sxs-lookup"><span data-stu-id="89911-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="89911-105">Die `SetPositions` -Methode legt die aktuelle Position und die Stoppposition fest.</span><span class="sxs-lookup"><span data-stu-id="89911-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="89911-106">Diese Methode implementiert die [**IMediaSeeking::SetPositions-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="89911-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89911-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89911-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="89911-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89911-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89911-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="89911-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="89911-110">Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeitformats angibt.</span><span class="sxs-lookup"><span data-stu-id="89911-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="89911-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="89911-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="89911-112">Bitweise Kombination von Flags.</span><span class="sxs-lookup"><span data-stu-id="89911-112">Bitwise combination of flags.</span></span> <span data-ttu-id="89911-113">Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="89911-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="89911-114">*Pstop*</span><span class="sxs-lookup"><span data-stu-id="89911-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="89911-115">Zeiger auf eine Variable, die die Beendigungszeit in Einheiten des aktuellen Zeitformats angibt.</span><span class="sxs-lookup"><span data-stu-id="89911-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="89911-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="89911-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="89911-117">Bitweise Kombination von Flags.</span><span class="sxs-lookup"><span data-stu-id="89911-117">Bitwise combination of flags.</span></span> <span data-ttu-id="89911-118">Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="89911-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89911-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89911-119">Return value</span></span>

<span data-ttu-id="89911-120">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="89911-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="89911-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89911-121">Requirements</span></span>



| <span data-ttu-id="89911-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89911-122">Requirement</span></span> | <span data-ttu-id="89911-123">Wert</span><span class="sxs-lookup"><span data-stu-id="89911-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89911-124">Header</span><span class="sxs-lookup"><span data-stu-id="89911-124">Header</span></span><br/>  | <dl> <span data-ttu-id="89911-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="89911-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89911-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89911-126">Library</span></span><br/> | <dl> <span data-ttu-id="89911-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="89911-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89911-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="89911-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89911-129">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="89911-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




