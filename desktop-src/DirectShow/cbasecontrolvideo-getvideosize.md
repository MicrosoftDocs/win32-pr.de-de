---
description: Die getvideosize-Methode ruft die Breite und Höhe des nativen Videos ab.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Cbasecontrolvideo. getvideosize-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372446"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="cd11a-103">Cbasecontrolvideo. getvideosize-Methode</span><span class="sxs-lookup"><span data-stu-id="cd11a-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="cd11a-104">Die `GetVideoSize` -Methode ruft die Breite und Höhe des nativen Videos ab.</span><span class="sxs-lookup"><span data-stu-id="cd11a-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd11a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd11a-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="cd11a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd11a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd11a-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="cd11a-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="cd11a-108">Zeiger auf die Video Breite.</span><span class="sxs-lookup"><span data-stu-id="cd11a-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="cd11a-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="cd11a-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="cd11a-110">Ein Zeiger auf die Video Höhe.</span><span class="sxs-lookup"><span data-stu-id="cd11a-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd11a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd11a-111">Return value</span></span>

<span data-ttu-id="cd11a-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd11a-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd11a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd11a-113">Requirements</span></span>



| <span data-ttu-id="cd11a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd11a-114">Requirement</span></span> | <span data-ttu-id="cd11a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cd11a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd11a-116">Header</span><span class="sxs-lookup"><span data-stu-id="cd11a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cd11a-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd11a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd11a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd11a-118">Library</span></span><br/> | <dl> <span data-ttu-id="cd11a-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cd11a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd11a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd11a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd11a-121">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd11a-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




