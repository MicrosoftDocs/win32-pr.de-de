---
description: Mit der setdefaulttargetrect-Methode wird das standardmäßige Ziel Video Rechteck (rein virtuell) festgelegt. Dies ist eine interne Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Cbasecontrolvideo. setdefaulttargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372079"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a><span data-ttu-id="eff0c-104">Cbasecontrolvideo. setdefaulttargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="eff0c-104">CBaseControlVideo.SetDefaultTargetRect method</span></span>

<span data-ttu-id="eff0c-105">Mit der- `SetDefaultTargetRect` Methode wird das standardmäßige Ziel Video Rechteck (rein virtuell) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eff0c-105">The `SetDefaultTargetRect` method sets the default target video rectangle (pure virtual).</span></span> <span data-ttu-id="eff0c-106">Dies ist eine interne Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eff0c-106">This is an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff0c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eff0c-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="eff0c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eff0c-108">Parameters</span></span>

<span data-ttu-id="eff0c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eff0c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eff0c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eff0c-110">Return value</span></span>

<span data-ttu-id="eff0c-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eff0c-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eff0c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eff0c-112">Remarks</span></span>

<span data-ttu-id="eff0c-113">Abgeleitete Klassen sollten diese überschreiben, um das Ziel Video Rechteck zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="eff0c-113">Derived classes should override this to reset the destination video rectangle.</span></span> <span data-ttu-id="eff0c-114">Sie wird von der [**cbasecontrolvideo:: setdefaultdestinationposition**](cbasecontrolvideo-setdefaultdestinationposition.md) -Member-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="eff0c-114">It is called from the [**CBaseControlVideo::SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) member function.</span></span>

<span data-ttu-id="eff0c-115">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eff0c-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



<span data-ttu-id="eff0c-116">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="eff0c-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="eff0c-117">Der m \_ MTiN-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**cmediatype**](cmediatype.md) -Objekt mit dem Medientyp der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="eff0c-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff0c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eff0c-118">Requirements</span></span>



| <span data-ttu-id="eff0c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eff0c-119">Requirement</span></span> | <span data-ttu-id="eff0c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eff0c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff0c-121">Header</span><span class="sxs-lookup"><span data-stu-id="eff0c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eff0c-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eff0c-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eff0c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eff0c-123">Library</span></span><br/> | <dl> <span data-ttu-id="eff0c-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eff0c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eff0c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eff0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff0c-126">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eff0c-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




