---
description: Die get \_ framesdroppedinrenderer-Methode ruft die Anzahl der Frames ab, die vom Renderer gelöscht wurden.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: CBaseVideoRenderer.get_FramesDroppedInRenderer-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370620"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="7a971-103">Cbasevideorenderer. get \_ framesdroppedinrenderer-Methode</span><span class="sxs-lookup"><span data-stu-id="7a971-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="7a971-104">Die- `get_FramesDroppedInRenderer` Methode ruft die Anzahl der Frames ab, die vom Renderer gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="7a971-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a971-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a971-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="7a971-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a971-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a971-107">*pcframesdrop*</span><span class="sxs-lookup"><span data-stu-id="7a971-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="7a971-108">Zeiger auf die Anzahl der gelöschten Frames.</span><span class="sxs-lookup"><span data-stu-id="7a971-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a971-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a971-109">Return value</span></span>

<span data-ttu-id="7a971-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a971-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a971-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a971-111">Remarks</span></span>

<span data-ttu-id="7a971-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ framesdroppedinrenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a971-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="7a971-113">Auf diese Weise Ruft die Eigenschaften Seite die Daten aus dem Scheduler ab.</span><span class="sxs-lookup"><span data-stu-id="7a971-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="7a971-114">Frames können auch Upstream abgelegt werden, ohne dass der Renderer Sie sehen kann.</span><span class="sxs-lookup"><span data-stu-id="7a971-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a971-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a971-115">Requirements</span></span>



| <span data-ttu-id="7a971-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a971-116">Requirement</span></span> | <span data-ttu-id="7a971-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7a971-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a971-118">Header</span><span class="sxs-lookup"><span data-stu-id="7a971-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7a971-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a971-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a971-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a971-120">Library</span></span><br/> | <dl> <span data-ttu-id="7a971-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7a971-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a971-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a971-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a971-123">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7a971-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




