---
description: Die setvariablesize-Methode gibt an, dass die Beispiele keine festgelegte Größe aufweisen.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Cmediatype. setvariablesize-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364470"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="33e1f-103">Cmediatype. setvariablesize-Methode</span><span class="sxs-lookup"><span data-stu-id="33e1f-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="33e1f-104">Die- `SetVariableSize` Methode gibt an, dass die-Beispiele keine festgelegte Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="33e1f-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e1f-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="33e1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33e1f-106">Parameters</span></span>

<span data-ttu-id="33e1f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="33e1f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33e1f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33e1f-108">Return value</span></span>

<span data-ttu-id="33e1f-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="33e1f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e1f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e1f-110">Remarks</span></span>

<span data-ttu-id="33e1f-111">Diese Methode legt das **bfixedsizesamples** -Element auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="33e1f-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="33e1f-112">Nachfolgende Aufrufe der [**cmediatype:: getSampleSize**](cmediatype-getsamplesize.md) -Methode geben 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="33e1f-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e1f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e1f-113">Requirements</span></span>



| <span data-ttu-id="33e1f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e1f-114">Requirement</span></span> | <span data-ttu-id="33e1f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="33e1f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e1f-116">Header</span><span class="sxs-lookup"><span data-stu-id="33e1f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="33e1f-117"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="33e1f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33e1f-118">Library</span></span><br/> | <dl> <span data-ttu-id="33e1f-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e1f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e1f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e1f-121">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33e1f-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




