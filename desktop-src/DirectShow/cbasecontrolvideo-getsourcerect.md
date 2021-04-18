---
description: Die getsourcerect-Methode ruft das Quell Rechteck ab. Dies ist eine interne Methode.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Cbasecontrolvideo. getsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372337"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="1a8b3-104">Cbasecontrolvideo. getsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="1a8b3-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="1a8b3-105">Die- `GetSourceRect` Methode ruft das Quell Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="1a8b3-106">Dies ist eine interne Methode.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8b3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a8b3-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="1a8b3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a8b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a8b3-109">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="1a8b3-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="1a8b3-110">Zeiger auf das abgerufene Quell Rechteck.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a8b3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a8b3-111">Return value</span></span>

<span data-ttu-id="1a8b3-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a8b3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a8b3-113">Remarks</span></span>

<span data-ttu-id="1a8b3-114">Diese Member-Funktion muss in der abgeleiteten Klasse überschrieben werden, um das vom Videorenderer gehaltene Quell Rechteck zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="1a8b3-115">Sie wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="1a8b3-116">**Cbasecontrolvideo:: getsourceposition**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="1a8b3-117">**Cbasecontrolvideo::p UT \_ sourceLeft**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="1a8b3-118">**Cbasecontrolvideo:: get \_ sourceLeft**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="1a8b3-119">**Cbasecontrolvideo::p UT \_ sourceWidth**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="1a8b3-120">**Cbasecontrolvideo:: get \_ sourceWidth**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="1a8b3-121">**Cbasecontrolvideo::p UT \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="1a8b3-122">**Cbasecontrolvideo:: get \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="1a8b3-123">**Cbasecontrolvideo::p UT \_ sourceHeight**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="1a8b3-124">**Cbasecontrolvideo:: get \_ sourceHeight**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="1a8b3-125">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="1a8b3-126">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1a8b3-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a8b3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a8b3-127">Requirements</span></span>



| <span data-ttu-id="1a8b3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a8b3-128">Requirement</span></span> | <span data-ttu-id="1a8b3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1a8b3-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8b3-130">Header</span><span class="sxs-lookup"><span data-stu-id="1a8b3-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8b3-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8b3-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a8b3-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a8b3-132">Library</span></span><br/> | <dl> <span data-ttu-id="1a8b3-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8b3-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a8b3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a8b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8b3-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a8b3-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




