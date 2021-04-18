---
description: Die isdefaultsourcerect-Methode bestimmt, ob der Renderer das standardmäßige Quell Rechteck (rein virtuell) verwendet.
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Cbasecontrolvideo. isdefaultsourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372445"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="da823-103">Cbasecontrolvideo. isdefaultsourcerect-Methode</span><span class="sxs-lookup"><span data-stu-id="da823-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="da823-104">Die- `IsDefaultSourceRect` Methode bestimmt, ob der Renderer das standardmäßige Quell Rechteck (rein virtuell) verwendet.</span><span class="sxs-lookup"><span data-stu-id="da823-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="da823-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da823-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="da823-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da823-106">Parameters</span></span>

<span data-ttu-id="da823-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="da823-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da823-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da823-108">Return value</span></span>

<span data-ttu-id="da823-109">Gibt s \_ OK zurück, wenn der Renderer die Standard Quelle verwendet; andernfalls wird s \_ false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da823-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="da823-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da823-110">Remarks</span></span>

<span data-ttu-id="da823-111">Diese Member-Funktion muss in der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="da823-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="da823-112">Sie wird von der [**cbasecontrolvideo:: isusingdefaultsource**](cbasecontrolvideo-isusingdefaultsource.md) -Member-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="da823-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="da823-113">Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="da823-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="da823-114">In diesem Beispiel ist cvideotext eine Klasse, die von [**cbasecontrolvideo**](cbasecontrolvideo.md)abgeleitet ist. m \_ prenderer enthält ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist, und das \_ in der abgeleiteten Klasse definierte Datenmember m DrawImage enthält ein [**cdrawimage**](cdrawimage.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="da823-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="da823-115">Der m \_ MTiN-Datenmember, der auch in der abgeleiteten Klasse definiert ist, enthält ein [**cmediatype**](cmediatype.md) -Objekt mit dem Medientyp der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="da823-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="da823-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da823-116">Requirements</span></span>



| <span data-ttu-id="da823-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da823-117">Requirement</span></span> | <span data-ttu-id="da823-118">Wert</span><span class="sxs-lookup"><span data-stu-id="da823-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da823-119">Header</span><span class="sxs-lookup"><span data-stu-id="da823-119">Header</span></span><br/>  | <dl> <span data-ttu-id="da823-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da823-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da823-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da823-121">Library</span></span><br/> | <dl> <span data-ttu-id="da823-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="da823-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da823-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da823-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da823-124">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="da823-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




