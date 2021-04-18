---
description: 'Die alterquality-Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird. Diese Methode überschreibt die ctransformfilter:: alterquality-Methode.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Cvideotransformfilter. alterquality-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365379"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="39acd-104">Cvideotransformfilter. alterquality-Methode</span><span class="sxs-lookup"><span data-stu-id="39acd-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="39acd-105">Die- `AlterQuality` Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="39acd-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="39acd-106">Diese Methode überschreibt die [**ctransformfilter:: alterquality**](ctransformfilter-alterquality.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="39acd-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39acd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39acd-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="39acd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39acd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39acd-109">*Q1*</span><span class="sxs-lookup"><span data-stu-id="39acd-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="39acd-110">[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="39acd-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39acd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39acd-111">Return value</span></span>

<span data-ttu-id="39acd-112">Gibt "E Fail" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="39acd-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="39acd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39acd-113">Remarks</span></span>

<span data-ttu-id="39acd-114">Diese Methode wird aufgerufen, wenn die Ausgabe-PIN eine Qualitäts Nachricht empfängt (durch die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode).</span><span class="sxs-lookup"><span data-stu-id="39acd-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="39acd-115">Der oder bei Verzögerung-Wert aus *q* wird in der **m \_ itrlate** -Member-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39acd-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="39acd-116">Der Rückgabewert von "E \_ Fail" gibt an, dass der Renderer durch das Ablegen von Frames auffangen soll, obwohl die **cvideotransformfilter** -Klasse auch Frames unter den richtigen Bedingungen ablegen wird.</span><span class="sxs-lookup"><span data-stu-id="39acd-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="39acd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39acd-117">Requirements</span></span>



| <span data-ttu-id="39acd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39acd-118">Requirement</span></span> | <span data-ttu-id="39acd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="39acd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39acd-120">Header</span><span class="sxs-lookup"><span data-stu-id="39acd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="39acd-121"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39acd-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="39acd-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39acd-122">Library</span></span><br/> | <dl> <span data-ttu-id="39acd-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="39acd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39acd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39acd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39acd-125">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="39acd-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="39acd-126">**Cvideotransformfilter:: schuldskipframe**</span><span class="sxs-lookup"><span data-stu-id="39acd-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




