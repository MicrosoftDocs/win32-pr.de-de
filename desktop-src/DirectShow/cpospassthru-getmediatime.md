---
description: Die getmediatime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Cpospassthru. getmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364602"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="f39f2-103">Cpospassthru. getmediatime-Methode</span><span class="sxs-lookup"><span data-stu-id="f39f2-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="f39f2-104">Die- `GetMediaTime` Methode ruft die Zeitstempel im aktuellen Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="f39f2-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f39f2-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="f39f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f39f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39f2-107">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="f39f2-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f39f2-108">Ein Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="f39f2-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="f39f2-109">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="f39f2-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f39f2-110">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="f39f2-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39f2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f39f2-111">Return value</span></span>

<span data-ttu-id="f39f2-112">Gibt "E Fail" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="f39f2-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f39f2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f39f2-113">Remarks</span></span>

<span data-ttu-id="f39f2-114">Überschreiben Sie diese Methode, wenn der Filter die Zeitstempel der empfangenen Beispiele zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="f39f2-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39f2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f39f2-115">Requirements</span></span>



| <span data-ttu-id="f39f2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f39f2-116">Requirement</span></span> | <span data-ttu-id="f39f2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f39f2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39f2-118">Header</span><span class="sxs-lookup"><span data-stu-id="f39f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f39f2-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f39f2-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f39f2-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f39f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="f39f2-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f39f2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f39f2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f39f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39f2-123">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f39f2-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




