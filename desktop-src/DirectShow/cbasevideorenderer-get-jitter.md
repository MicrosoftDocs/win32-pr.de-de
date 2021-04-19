---
description: Die get \_ Jitter-Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen den einzelnen Frames und der nächsten für alle Frames ab, seit das Streaming gestartet wurde.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: CBaseVideoRenderer.get_Jitter-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356397"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="8d1f9-103">Cbasevideorenderer. get \_ Jitter-Methode</span><span class="sxs-lookup"><span data-stu-id="8d1f9-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="8d1f9-104">Die `get_Jitter` -Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen den einzelnen Frames und der nächsten für alle Frames ab, seit das Streaming gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d1f9-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="8d1f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d1f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1f9-107">*pijitter*</span><span class="sxs-lookup"><span data-stu-id="8d1f9-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="8d1f9-108">Ein Zeiger auf die Standardabweichung der Interframe-Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d1f9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d1f9-109">Return value</span></span>

<span data-ttu-id="8d1f9-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1f9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d1f9-111">Remarks</span></span>

<span data-ttu-id="8d1f9-112">Diese Member-Funktion implementiert die [**iqualprop:: get \_ Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8d1f9-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1f9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d1f9-113">Requirements</span></span>



| <span data-ttu-id="8d1f9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d1f9-114">Requirement</span></span> | <span data-ttu-id="8d1f9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8d1f9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1f9-116">Header</span><span class="sxs-lookup"><span data-stu-id="8d1f9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8d1f9-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d1f9-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d1f9-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8d1f9-118">Library</span></span><br/> | <dl> <span data-ttu-id="8d1f9-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8d1f9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d1f9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d1f9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1f9-121">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8d1f9-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




