---
title: D1110 Flush-Fehler
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Fehler beim Flush-Befehl durch ein Renderziel.
keywords:
- D1110 Flush-Fehler Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390987"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="da1b2-104">D1110: Fehler beim leeren.</span><span class="sxs-lookup"><span data-stu-id="da1b2-104">D1110: Flush Failure</span></span>

<span data-ttu-id="da1b2-105">Ein Flush-Befehl von einer fehlerhaften Renderziel \[ *Ressource* \] .</span><span class="sxs-lookup"><span data-stu-id="da1b2-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="da1b2-106">Tags \[ *Tag1*, *Tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="da1b2-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="da1b2-107">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="da1b2-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="da1b2-108"><span id="resource"></span><span id="RESOURCE"></span>*Ressource*</span><span class="sxs-lookup"><span data-stu-id="da1b2-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="da1b2-109">Die Adresse des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="da1b2-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="da1b2-110"><span id="tag1"></span><span id="TAG1"></span>*Tag1*</span><span class="sxs-lookup"><span data-stu-id="da1b2-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="da1b2-111">Der erste Tagwert.</span><span class="sxs-lookup"><span data-stu-id="da1b2-111">The first tag value.</span></span> <span data-ttu-id="da1b2-112">Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="da1b2-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="da1b2-113"><span id="tag2"></span><span id="TAG2"></span>*Tag2*</span><span class="sxs-lookup"><span data-stu-id="da1b2-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="da1b2-114">Der zweite Tagwert.</span><span class="sxs-lookup"><span data-stu-id="da1b2-114">The second tag value.</span></span> <span data-ttu-id="da1b2-115">Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="da1b2-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="da1b2-116">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="da1b2-116">Error Level</span></span> | <span data-ttu-id="da1b2-117">Warnung</span><span class="sxs-lookup"><span data-stu-id="da1b2-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="da1b2-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da1b2-118">Examples</span></span>

<span data-ttu-id="da1b2-119">**Beispiel 1:** Der folgende Code zeigt, dass sich ein Draw-Befehl in einem ungültigen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="da1b2-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="da1b2-120">Um die Warnmeldung zu vermeiden, verwenden Sie [**setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , um den D2D1 \_ Antialias \_ Modus- \_ Antialiasing vor einem [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Befehl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="da1b2-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="da1b2-121">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="da1b2-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="da1b2-122">**Beispiel 2:** Der folgende Code zeigt, dass das leeren nach dem [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Aufruf [**aufgerufen wird.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)</span><span class="sxs-lookup"><span data-stu-id="da1b2-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="da1b2-123">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="da1b2-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="da1b2-124">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="da1b2-124">Possible Causes</span></span>

<span data-ttu-id="da1b2-125">Der [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) -Befehl kann aus zwei Gründen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="da1b2-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="da1b2-126">Möglicherweise tritt ein Fehler auf, weil die Methode außerhalb des [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)- / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Aufrufs aufgerufen wurde, oder es kann zu einem Fehler kommen, weil ein Fehler von einem der renderzielvorgänge  verursacht wurde, die seit dem letzten Löschvorgang oder **EndDraw** -Aufruf verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="da1b2-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="da1b2-127">Um das Problem zu beheben, sollte die Anwendung die Ursache des Fehlers ermitteln und die entsprechende Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="da1b2-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="da1b2-128">Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="da1b2-128">Fixes</span></span>

<span data-ttu-id="da1b2-129">Es gibt viele Gründe, warum ein [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) -Befehl fehlschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="da1b2-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="da1b2-130">Die Anwendung sollte die Ursache des Fehlers ermitteln und die entsprechende Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="da1b2-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 