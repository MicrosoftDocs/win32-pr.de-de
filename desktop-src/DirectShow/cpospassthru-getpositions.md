---
description: 'Die getpositions-Methode ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaseeking:: getpositions-Methode.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Cpospassthru. getpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371205"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="ca92a-104">Cpospassthru. getpositions-Methode</span><span class="sxs-lookup"><span data-stu-id="ca92a-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="ca92a-105">Die `GetPositions` -Methode ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="ca92a-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="ca92a-106">Diese Methode implementiert die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ca92a-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca92a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca92a-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="ca92a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca92a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca92a-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="ca92a-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="ca92a-110">Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca92a-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="ca92a-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="ca92a-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ca92a-112">Ein Zeiger auf eine Variable, die die Position des Stopps in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca92a-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca92a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca92a-113">Return value</span></span>

<span data-ttu-id="ca92a-114">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="ca92a-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca92a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca92a-115">Requirements</span></span>



| <span data-ttu-id="ca92a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca92a-116">Requirement</span></span> | <span data-ttu-id="ca92a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ca92a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92a-118">Header</span><span class="sxs-lookup"><span data-stu-id="ca92a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ca92a-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca92a-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca92a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca92a-120">Library</span></span><br/> | <dl> <span data-ttu-id="ca92a-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca92a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca92a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca92a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca92a-123">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ca92a-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




