---
description: Mit der setsourcerect-Methode wird das aktuelle Quellvideo Rechteck (rein virtuell) festgelegt. Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Quell Rechteck geändert wird.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Cbasecontrolvideo. setsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366883"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="c932c-104">Cbasecontrolvideo. setsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="c932c-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="c932c-105">Die- `SetSourceRect` Methode legt das aktuelle Quellvideo Rechteck (rein virtuell) fest.</span><span class="sxs-lookup"><span data-stu-id="c932c-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="c932c-106">Dabei handelt es sich um eine interne Member-Funktion, die aufgerufen wird, wenn das Quell Rechteck geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c932c-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c932c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c932c-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c932c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c932c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c932c-109">*psourcerect*</span><span class="sxs-lookup"><span data-stu-id="c932c-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="c932c-110">Zeiger auf das Quell Rechteck.</span><span class="sxs-lookup"><span data-stu-id="c932c-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c932c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c932c-111">Return value</span></span>

<span data-ttu-id="c932c-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c932c-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c932c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c932c-113">Remarks</span></span>

<span data-ttu-id="c932c-114">Abgeleitete Klassen sollten diese Member-Funktion überschreiben, um zu ermitteln, wann das Quell Rechteck geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c932c-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="c932c-115">Sie wird von den folgenden Member-Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c932c-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="c932c-116">**Cbasecontrolvideo:: setsourceposition**</span><span class="sxs-lookup"><span data-stu-id="c932c-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="c932c-117">**Cbasecontrolvideo::p UT \_ sourceLeft**</span><span class="sxs-lookup"><span data-stu-id="c932c-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="c932c-118">**Cbasecontrolvideo::p UT \_ sourceWidth**</span><span class="sxs-lookup"><span data-stu-id="c932c-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="c932c-119">**Cbasecontrolvideo::p UT \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="c932c-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="c932c-120">**Cbasecontrolvideo::p UT \_ sourceHeight**</span><span class="sxs-lookup"><span data-stu-id="c932c-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="c932c-121">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c932c-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="c932c-122">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c932c-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c932c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c932c-123">Requirements</span></span>



| <span data-ttu-id="c932c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c932c-124">Requirement</span></span> | <span data-ttu-id="c932c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c932c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c932c-126">Header</span><span class="sxs-lookup"><span data-stu-id="c932c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c932c-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c932c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c932c-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c932c-128">Library</span></span><br/> | <dl> <span data-ttu-id="c932c-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c932c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c932c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c932c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c932c-131">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c932c-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




