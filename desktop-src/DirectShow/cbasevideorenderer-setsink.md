---
description: Die setsink-Methode legt das iqualitycontrol-Objekt fest, das Qualitäts Meldungen empfängt.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Cbasevideorenderer. setsink-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351205"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="e237b-103">Cbasevideorenderer. setsink-Methode</span><span class="sxs-lookup"><span data-stu-id="e237b-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="e237b-104">Die- `SetSink` Methode legt das [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Objekt fest, das Qualitäts Meldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="e237b-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="e237b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e237b-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="e237b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e237b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e237b-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="e237b-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="e237b-108">Zeiger auf das [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Objekt, an das die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e237b-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e237b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e237b-109">Return value</span></span>

<span data-ttu-id="e237b-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e237b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e237b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e237b-111">Remarks</span></span>

<span data-ttu-id="e237b-112">Diese Member-Funktion implementiert die [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) -Methode für den Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="e237b-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e237b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e237b-113">Requirements</span></span>



| <span data-ttu-id="e237b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e237b-114">Requirement</span></span> | <span data-ttu-id="e237b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e237b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e237b-116">Header</span><span class="sxs-lookup"><span data-stu-id="e237b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e237b-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e237b-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e237b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e237b-118">Library</span></span><br/> | <dl> <span data-ttu-id="e237b-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e237b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e237b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e237b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e237b-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e237b-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




