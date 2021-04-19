---
description: 'Die getstoppositionelle-Methode ruft die Zeit ab, zu der die Wiedergabe in Bezug auf die Dauer des Streams beendet wird. Diese Methode implementiert die imediaseeking:: getstoppositionelle-Methode.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Csourceseeking. getstoppositionelle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351381"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="075ff-104">Csourceseeking. getstoppositionelle-Methode</span><span class="sxs-lookup"><span data-stu-id="075ff-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="075ff-105">Die- `GetStopPosition` Methode ruft die Zeit ab, zu der die Wiedergabe in Bezug auf die Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="075ff-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="075ff-106">Diese Methode implementiert die [**imediaseeking:: getstoppositionelle**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="075ff-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="075ff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="075ff-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="075ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="075ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075ff-109">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="075ff-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="075ff-110">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="075ff-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075ff-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="075ff-111">Return value</span></span>

<span data-ttu-id="075ff-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="075ff-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="075ff-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="075ff-113">Return code</span></span>                                                                               | <span data-ttu-id="075ff-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="075ff-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="075ff-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="075ff-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="075ff-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="075ff-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="075ff-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="075ff-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="075ff-118">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="075ff-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="075ff-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="075ff-119">Remarks</span></span>

<span data-ttu-id="075ff-120">Die Endzeit wird von der Element Variablen [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="075ff-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="075ff-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="075ff-121">Requirements</span></span>



| <span data-ttu-id="075ff-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="075ff-122">Requirement</span></span> | <span data-ttu-id="075ff-123">Wert</span><span class="sxs-lookup"><span data-stu-id="075ff-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075ff-124">Header</span><span class="sxs-lookup"><span data-stu-id="075ff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="075ff-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="075ff-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="075ff-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="075ff-126">Library</span></span><br/> | <dl> <span data-ttu-id="075ff-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="075ff-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="075ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075ff-129">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="075ff-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




