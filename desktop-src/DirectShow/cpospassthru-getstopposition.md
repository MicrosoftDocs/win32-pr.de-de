---
description: 'Die getstoppositionelle-Methode ruft die Zeit ab, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die imediaseeking:: getstoppositionelle-Methode.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Cpospassthru. getstoppositionelle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364534"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="a3dda-104">Cpospassthru. getstoppositionelle-Methode</span><span class="sxs-lookup"><span data-stu-id="a3dda-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="a3dda-105">Die- `GetStopPosition` Methode ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3dda-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="a3dda-106">Diese Methode implementiert die [**imediaseeking:: getstoppositionelle**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3dda-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dda-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3dda-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="a3dda-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3dda-109">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="a3dda-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dda-110">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="a3dda-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3dda-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3dda-111">Return value</span></span>

<span data-ttu-id="a3dda-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="a3dda-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3dda-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3dda-113">Requirements</span></span>



| <span data-ttu-id="a3dda-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3dda-114">Requirement</span></span> | <span data-ttu-id="a3dda-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a3dda-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dda-116">Header</span><span class="sxs-lookup"><span data-stu-id="a3dda-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a3dda-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3dda-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3dda-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3dda-118">Library</span></span><br/> | <dl> <span data-ttu-id="a3dda-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3dda-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3dda-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3dda-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dda-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a3dda-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




