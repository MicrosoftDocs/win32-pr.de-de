---
description: Die settargetrect-Methode legt das aktuelle Ziel Rechteck (rein virtuell) fest. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Ziel Rechteck geändert wird.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Cbasecontrolvideo. settargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366882"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="89b04-104">Cbasecontrolvideo. settargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="89b04-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="89b04-105">Die- `SetTargetRect` Methode legt das aktuelle Ziel Rechteck (rein virtuell) fest.</span><span class="sxs-lookup"><span data-stu-id="89b04-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="89b04-106">Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Ziel Rechteck geändert wird.</span><span class="sxs-lookup"><span data-stu-id="89b04-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b04-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b04-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="89b04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89b04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b04-109">*ptargetrect*</span><span class="sxs-lookup"><span data-stu-id="89b04-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="89b04-110">Zeiger auf das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="89b04-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b04-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89b04-111">Return value</span></span>

<span data-ttu-id="89b04-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89b04-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89b04-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89b04-113">Remarks</span></span>

<span data-ttu-id="89b04-114">Abgeleitete Klassen sollten diese überschreiben, um zu ermitteln, wann das Ziel Rechteck geändert wird.</span><span class="sxs-lookup"><span data-stu-id="89b04-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="89b04-115">Sie wird von den folgenden Member-Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="89b04-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="89b04-116">**Cbasecontrolvideo:: setdestinationposition**</span><span class="sxs-lookup"><span data-stu-id="89b04-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="89b04-117">**Cbasecontrolvideo::p UT \_ destinationleft**</span><span class="sxs-lookup"><span data-stu-id="89b04-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="89b04-118">**Cbasecontrolvideo::p UT \_ destinationwidth**</span><span class="sxs-lookup"><span data-stu-id="89b04-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="89b04-119">**Cbasecontrolvideo::p UT \_ destinationtop**</span><span class="sxs-lookup"><span data-stu-id="89b04-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="89b04-120">**Cbasecontrolvideo::p UT \_ destinationheight**</span><span class="sxs-lookup"><span data-stu-id="89b04-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="89b04-121">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="89b04-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="89b04-122">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89b04-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b04-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89b04-123">Requirements</span></span>



| <span data-ttu-id="89b04-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89b04-124">Requirement</span></span> | <span data-ttu-id="89b04-125">Wert</span><span class="sxs-lookup"><span data-stu-id="89b04-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b04-126">Header</span><span class="sxs-lookup"><span data-stu-id="89b04-126">Header</span></span><br/>  | <dl> <span data-ttu-id="89b04-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89b04-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89b04-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89b04-128">Library</span></span><br/> | <dl> <span data-ttu-id="89b04-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="89b04-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b04-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89b04-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b04-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="89b04-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




