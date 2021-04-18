---
description: Reine virtuelle Methode, die abgeleitete Klassen überschreiben.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Cbasecontrolvideo. getstaticimage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365475"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="d76ea-103">Cbasecontrolvideo. getstaticimage-Methode</span><span class="sxs-lookup"><span data-stu-id="d76ea-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="d76ea-104">Reine virtuelle Methode, die abgeleitete Klassen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d76ea-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d76ea-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d76ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d76ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76ea-107">*pbuffersize*</span><span class="sxs-lookup"><span data-stu-id="d76ea-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-108">Ein Zeiger auf die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="d76ea-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d76ea-109">*pdibimage*</span><span class="sxs-lookup"><span data-stu-id="d76ea-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-110">Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="d76ea-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d76ea-111">Return value</span></span>

<span data-ttu-id="d76ea-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d76ea-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d76ea-113">Remarks</span></span>

<span data-ttu-id="d76ea-114">Mithilfe der [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle kann eine Anwendung anfordern, dass Sie eine Kopie des aktuellen Bilds in einem Arbeitsspeicher Puffer erhält (einige Renderer können E \_ notimpl zurückgeben, wenn Sie Sie nicht unterstützen).</span><span class="sxs-lookup"><span data-stu-id="d76ea-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="d76ea-115">Die abgeleitete Klasse bestimmt, wie das Bild abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d76ea-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="d76ea-116">Wenn die Anwendung **cbasecontrolvideo:: getstaticimage** aufruft, ruft Sie diese rein virtuelle Methode auf, die von der abgeleiteten Klasse überschrieben werden soll, um Sie zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d76ea-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="d76ea-117">Dies wird auch durch die Member-Funktion [**cbasecontrolvideo:: Get-timage**](cbasecontrolvideo-getcurrentimage.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d76ea-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="d76ea-118">Die-Klasse stellt eine Hilfsmember-Funktion, [**cbasecontrolvideo:: CopyImage**](cbasecontrolvideo-copyimage.md), bereit, die ein Beispiel erhalten kann, das ein Bild enthält, und die Member-Funktion kopiert den relevanten Abschnitt des Elements (auf Grundlage des aktuellen Quell Rechtecks) in den von der Anwendung bereitgestellten Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="d76ea-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="d76ea-119">Im folgenden Beispiel wird eine Implementierung dieser Member-Funktion in einer abgeleiteten Klasse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d76ea-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="d76ea-120">In diesem Beispiel \_ enthält der m-prenderer ein Objekt einer Klasse, die von [**cbasevideorenderer**](cbasevideorenderer.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="d76ea-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d76ea-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d76ea-121">Requirements</span></span>



| <span data-ttu-id="d76ea-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d76ea-122">Requirement</span></span> | <span data-ttu-id="d76ea-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d76ea-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76ea-124">Header</span><span class="sxs-lookup"><span data-stu-id="d76ea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d76ea-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d76ea-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d76ea-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d76ea-126">Library</span></span><br/> | <dl> <span data-ttu-id="d76ea-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d76ea-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d76ea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d76ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76ea-129">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d76ea-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




