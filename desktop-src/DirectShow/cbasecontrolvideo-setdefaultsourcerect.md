---
description: Mit der setdefaultsourcerect-Methode wird das standardmäßige Quellvideo Rechteck (rein virtuell) festgelegt. Dies in einer internen Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Cbasecontrolvideo. setdefaultsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351393"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="006f2-104">Cbasecontrolvideo. setdefaultsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="006f2-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="006f2-105">Die- `SetDefaultSourceRect` Methode legt das standardmäßige Quellvideo Rechteck (rein virtuell) fest.</span><span class="sxs-lookup"><span data-stu-id="006f2-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="006f2-106">Dies in einer internen Member-Funktion, die beim Zurücksetzen des Quell Rechtecks aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="006f2-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="006f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="006f2-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="006f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="006f2-108">Parameters</span></span>

<span data-ttu-id="006f2-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="006f2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="006f2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="006f2-110">Return value</span></span>

<span data-ttu-id="006f2-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="006f2-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="006f2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="006f2-112">Remarks</span></span>

<span data-ttu-id="006f2-113">Abgeleitete Klassen sollten diese überschreiben, um das Quell Rechteck zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="006f2-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="006f2-114">Sie wird von [**cbasecontrolvideo:: setdefaultsourceposition**](cbasecontrolvideo-setdefaultsourceposition.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="006f2-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="006f2-115">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="006f2-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="006f2-116">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="006f2-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="006f2-117">Der m \_ MTiN-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**cmediatype**](cmediatype.md) -Objekt mit dem Medientyp der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="006f2-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="006f2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="006f2-118">Requirements</span></span>



| <span data-ttu-id="006f2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="006f2-119">Requirement</span></span> | <span data-ttu-id="006f2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="006f2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006f2-121">Header</span><span class="sxs-lookup"><span data-stu-id="006f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="006f2-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="006f2-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="006f2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="006f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="006f2-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="006f2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="006f2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="006f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006f2-126">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="006f2-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




