---
description: Die schedulesample-Methode überschreibt die Basisklasse, die die Hauptarbeit durchführt, um die Anzahl der gezeichneten und gelöschten Stichproben zu erhalten (die von der iqualprop-Implementierung verwendet werden).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Cbasevideorenderer. schedulesample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369419"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="5a29f-103">Cbasevideorenderer. schedulesample-Methode</span><span class="sxs-lookup"><span data-stu-id="5a29f-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="5a29f-104">Die- `ScheduleSample` Methode überschreibt die Basisklasse, die die Hauptarbeit durchführt, um die Anzahl der gezeichneten und gelöschten Stichproben zu erhalten (die von der [**iqualprop**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) -Implementierung verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="5a29f-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a29f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a29f-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="5a29f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a29f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a29f-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="5a29f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5a29f-108">Zeiger auf das Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5a29f-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a29f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a29f-109">Return value</span></span>

<span data-ttu-id="5a29f-110">Gibt " **true** " zurück, wenn das Beispiel geplant ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a29f-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a29f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a29f-111">Requirements</span></span>



| <span data-ttu-id="5a29f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a29f-112">Requirement</span></span> | <span data-ttu-id="5a29f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5a29f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a29f-114">Header</span><span class="sxs-lookup"><span data-stu-id="5a29f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5a29f-115"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a29f-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a29f-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a29f-116">Library</span></span><br/> | <dl> <span data-ttu-id="5a29f-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5a29f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a29f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a29f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a29f-119">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5a29f-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




