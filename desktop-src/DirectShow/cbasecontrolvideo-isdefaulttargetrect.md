---
description: Die isdefaulttargetrect-Methode bestimmt, ob der Renderer das standardmäßige Ziel Rechteck (rein virtuell) verwendet.
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Cbasecontrolvideo. isdefaulttargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360447"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="2d7a2-103">Cbasecontrolvideo. isdefaulttargetrect-Methode</span><span class="sxs-lookup"><span data-stu-id="2d7a2-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="2d7a2-104">Die- `IsDefaultTargetRect` Methode bestimmt, ob der Renderer das standardmäßige Ziel Rechteck (rein virtuell) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d7a2-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="2d7a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d7a2-106">Parameters</span></span>

<span data-ttu-id="2d7a2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d7a2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d7a2-108">Return value</span></span>

<span data-ttu-id="2d7a2-109">Gibt s \_ OK zurück, wenn der Renderer das Standardziel verwendet; andernfalls wird s \_ false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d7a2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d7a2-110">Remarks</span></span>

<span data-ttu-id="2d7a2-111">Diese Member-Funktion muss in der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="2d7a2-112">Sie wird von der [**cbasecontrolvideo:: isusingdefaultdestination**](cbasecontrolvideo-isusingdefaultdestination.md) -Member-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="2d7a2-113">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="2d7a2-114">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="2d7a2-115">Der m \_ MTiN-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**cmediatype**](cmediatype.md) -Objekt mit dem Medientyp der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="2d7a2-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7a2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d7a2-116">Requirements</span></span>



| <span data-ttu-id="2d7a2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d7a2-117">Requirement</span></span> | <span data-ttu-id="2d7a2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2d7a2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7a2-119">Header</span><span class="sxs-lookup"><span data-stu-id="2d7a2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2d7a2-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d7a2-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d7a2-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d7a2-121">Library</span></span><br/> | <dl> <span data-ttu-id="2d7a2-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d7a2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d7a2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d7a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7a2-124">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2d7a2-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




