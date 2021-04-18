---
description: Die get \_ avgframerate-Methode berechnet die durchschnittliche Frame Rate und ruft Sie ab.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: CBaseVideoRenderer.get_AvgFrameRate-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365592"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="7f30f-103">Cbasevideorenderer. get \_ avgframerate-Methode</span><span class="sxs-lookup"><span data-stu-id="7f30f-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="7f30f-104">Die `get_AvgFrameRate` -Methode berechnet die durchschnittliche Framerate und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="7f30f-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f30f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f30f-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="7f30f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f30f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f30f-107">*piavgframerate*</span><span class="sxs-lookup"><span data-stu-id="7f30f-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="7f30f-108">Zeiger auf die Anzahl von Frames pro Sekunde, seit das Streaming begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="7f30f-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f30f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f30f-109">Return value</span></span>

<span data-ttu-id="7f30f-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f30f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f30f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f30f-111">Remarks</span></span>

<span data-ttu-id="7f30f-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ avgframerate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7f30f-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f30f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f30f-113">Requirements</span></span>



| <span data-ttu-id="7f30f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f30f-114">Requirement</span></span> | <span data-ttu-id="7f30f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7f30f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f30f-116">Header</span><span class="sxs-lookup"><span data-stu-id="7f30f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7f30f-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f30f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f30f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f30f-118">Library</span></span><br/> | <dl> <span data-ttu-id="7f30f-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f30f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f30f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f30f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f30f-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f30f-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




