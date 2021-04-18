---
description: Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Nicht implementiert.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Csourceseeking. GetCurrentPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361316"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="460c8-104">Csourceseeking. GetCurrentPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="460c8-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="460c8-105">Die- `GetCurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="460c8-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="460c8-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="460c8-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="460c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="460c8-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="460c8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="460c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460c8-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="460c8-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="460c8-110">Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="460c8-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460c8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="460c8-111">Return value</span></span>

<span data-ttu-id="460c8-112">Gibt "E \_ notimpl" zurück.</span><span class="sxs-lookup"><span data-stu-id="460c8-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="460c8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="460c8-113">Remarks</span></span>

<span data-ttu-id="460c8-114">Quell Filter unterstützen diese Methode in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="460c8-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="460c8-115">Stattdessen melden rendererfilter die aktuelle Position über die [**crendererpospassthru**](crendererpospassthru.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="460c8-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="460c8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="460c8-116">Requirements</span></span>



| <span data-ttu-id="460c8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="460c8-117">Requirement</span></span> | <span data-ttu-id="460c8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="460c8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460c8-119">Header</span><span class="sxs-lookup"><span data-stu-id="460c8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="460c8-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="460c8-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="460c8-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="460c8-121">Library</span></span><br/> | <dl> <span data-ttu-id="460c8-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="460c8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="460c8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="460c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460c8-124">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="460c8-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




