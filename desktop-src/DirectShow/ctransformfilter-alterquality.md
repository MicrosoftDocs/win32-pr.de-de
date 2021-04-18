---
description: Die alterquality-Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Ctransformfilter. alterquality-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364843"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="0df0b-103">Ctransformfilter. alterquality-Methode</span><span class="sxs-lookup"><span data-stu-id="0df0b-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="0df0b-104">Die- `AlterQuality` Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0df0b-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0df0b-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="0df0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0df0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df0b-107">*Q1*</span><span class="sxs-lookup"><span data-stu-id="0df0b-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="0df0b-108">[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="0df0b-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df0b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0df0b-109">Return value</span></span>

<span data-ttu-id="0df0b-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0df0b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0df0b-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0df0b-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0df0b-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0df0b-112">Return code</span></span>                                                                             | <span data-ttu-id="0df0b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0df0b-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0df0b-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0b-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0df0b-115">Die Qualitäts Meldung konnte nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0df0b-115">Did not handle the quality message.</span></span> <span data-ttu-id="0df0b-116">Die Nachricht sollte per Upstream übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="0df0b-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="0df0b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0b-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0df0b-118">Die Qualitäts Meldung wurde verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0df0b-118">Handled the quality message.</span></span> <span data-ttu-id="0df0b-119">Es sind keine weiteren Aktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0df0b-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="0df0b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0df0b-120">Remarks</span></span>

<span data-ttu-id="0df0b-121">Überschreiben Sie diese Methode, wenn der Filter die Qualitätskontrolle ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="0df0b-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="0df0b-122">Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="0df0b-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0df0b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0df0b-123">Requirements</span></span>



| <span data-ttu-id="0df0b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0df0b-124">Requirement</span></span> | <span data-ttu-id="0df0b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0df0b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df0b-126">Header</span><span class="sxs-lookup"><span data-stu-id="0df0b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0df0b-127"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0df0b-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0df0b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0df0b-128">Library</span></span><br/> | <dl> <span data-ttu-id="0df0b-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0df0b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df0b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0df0b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df0b-131">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0df0b-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




