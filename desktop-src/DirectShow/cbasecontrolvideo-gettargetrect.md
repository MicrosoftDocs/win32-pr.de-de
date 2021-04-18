---
description: Die gettargetrect-Methode ruft das Ziel Rechteck ab. Dies ist eine interne Hilfsmember-Funktion.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Cbasecontrolvideo. gettargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364952"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="904aa-104">Cbasecontrolvideo. gettargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="904aa-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="904aa-105">Die- `GetTargetRect` Methode ruft das Ziel Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="904aa-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="904aa-106">Dies ist eine interne Hilfsmember-Funktion.</span><span class="sxs-lookup"><span data-stu-id="904aa-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="904aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="904aa-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="904aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="904aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904aa-109">*ptargetrect*</span><span class="sxs-lookup"><span data-stu-id="904aa-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="904aa-110">Zeiger auf das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="904aa-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="904aa-111">Return value</span></span>

<span data-ttu-id="904aa-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="904aa-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="904aa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="904aa-113">Remarks</span></span>

<span data-ttu-id="904aa-114">Diese Member-Funktion muss in der abgeleiteten Klasse überschrieben werden, um das Ziel Rechteck zurückzugeben, das der Videorenderer innehat.</span><span class="sxs-lookup"><span data-stu-id="904aa-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="904aa-115">Sie wird von den folgenden [**cbasecontrolvideo**](cbasecontrolvideo.md) -Element Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="904aa-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="904aa-116">**Cbasecontrolvideo:: getdestinationposition**</span><span class="sxs-lookup"><span data-stu-id="904aa-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="904aa-117">**Cbasecontrolvideo::p UT \_ destinationleft**</span><span class="sxs-lookup"><span data-stu-id="904aa-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="904aa-118">**Cbasecontrolvideo:: get \_ destinationleft**</span><span class="sxs-lookup"><span data-stu-id="904aa-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="904aa-119">**Cbasecontrolvideo::p UT \_ destinationwidth**</span><span class="sxs-lookup"><span data-stu-id="904aa-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="904aa-120">**Cbasecontrolvideo:: get \_ destinationwidth**</span><span class="sxs-lookup"><span data-stu-id="904aa-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="904aa-121">**Cbasecontrolvideo::p UT \_ destinationtop**</span><span class="sxs-lookup"><span data-stu-id="904aa-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="904aa-122">**Cbasecontrolvideo:: get \_ destinationtop**</span><span class="sxs-lookup"><span data-stu-id="904aa-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="904aa-123">**Cbasecontrolvideo::p UT \_ destinationheight**</span><span class="sxs-lookup"><span data-stu-id="904aa-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="904aa-124">**Cbasecontrolvideo:: get \_ destinationheight**</span><span class="sxs-lookup"><span data-stu-id="904aa-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="904aa-125">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="904aa-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="904aa-126">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="904aa-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="904aa-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="904aa-127">Requirements</span></span>



| <span data-ttu-id="904aa-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="904aa-128">Requirement</span></span> | <span data-ttu-id="904aa-129">Wert</span><span class="sxs-lookup"><span data-stu-id="904aa-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904aa-130">Header</span><span class="sxs-lookup"><span data-stu-id="904aa-130">Header</span></span><br/>  | <dl> <span data-ttu-id="904aa-131"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="904aa-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="904aa-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="904aa-132">Library</span></span><br/> | <dl> <span data-ttu-id="904aa-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="904aa-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904aa-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="904aa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904aa-135">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="904aa-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




