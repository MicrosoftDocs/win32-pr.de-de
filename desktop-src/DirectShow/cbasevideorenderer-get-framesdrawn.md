---
description: Die get \_ framesgezeichnet-Methode ruft die m \_ cframesdrawn-Element Variable ab und gibt so die Anzahl der Rahmen an, die seit dem Start des Streaming gezeichnet wurden.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get_FramesDrawn-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371035"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="13c35-103">Cbasevideorenderer. get \_ framesgezeichnet-Methode</span><span class="sxs-lookup"><span data-stu-id="13c35-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="13c35-104">Die- `get_FramesDrawn` Methode ruft die **m \_ cframesdrawn** -Element Variable ab und gibt die Anzahl der Rahmen an, die seit dem Start des Streamings gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="13c35-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13c35-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="13c35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13c35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c35-107">*pcframesdrawn*</span><span class="sxs-lookup"><span data-stu-id="13c35-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="13c35-108">Ein Zeiger auf die Anzahl der gezeichneten Frames.</span><span class="sxs-lookup"><span data-stu-id="13c35-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c35-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13c35-109">Return value</span></span>

<span data-ttu-id="13c35-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="13c35-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c35-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13c35-111">Remarks</span></span>

<span data-ttu-id="13c35-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ framesgezeichnet**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) -Methode.</span><span class="sxs-lookup"><span data-stu-id="13c35-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c35-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13c35-113">Requirements</span></span>



| <span data-ttu-id="13c35-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13c35-114">Requirement</span></span> | <span data-ttu-id="13c35-115">Wert</span><span class="sxs-lookup"><span data-stu-id="13c35-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c35-116">Header</span><span class="sxs-lookup"><span data-stu-id="13c35-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13c35-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13c35-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13c35-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13c35-118">Library</span></span><br/> | <dl> <span data-ttu-id="13c35-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="13c35-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c35-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c35-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c35-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="13c35-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




