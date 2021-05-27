---
title: D1110– Leerungsfehler
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Fehler beim Flush-Aufruf eines Renderziels
keywords:
- D1110 Flush Failure Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549925"
---
# <a name="d1110-flush-failure"></a>D1110: Leerungsfehler

Ein Flush-Aufruf durch eine fehlerhafte \[ *Renderzielressource.* \] Tags \[ *tag1,* *tag2* \] .

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse des Renderziels.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Der erste Tagwert. Weitere Informationen finden Sie unter [**SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Der zweite Tagwert. Weitere Informationen finden Sie unter [**SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="examples"></a>Beispiele

**Beispiel 1:** Der folgende Code zeigt, dass sich ein Draw-Aufruf in einem ungültigen Zustand befindet. Um die Warnmeldung zu vermeiden, verwenden Sie [**SetAntialiasMode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) um D2D1 \_ ANTIALIAS MODE ANTIALIASED vor einem \_ \_ [**FillOpacityMask-Aufruf**](id2d1rendertarget-fillopacitymask.md) zu setzen.


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





In diesem Beispiel wird die folgende Debugmeldung erzeugt:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Beispiel 2:** Der folgende Code zeigt, dass [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) nach dem [**EndDraw-Aufruf aufgerufen**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) wird.


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



In diesem Beispiel wird die folgende Debugmeldung erzeugt:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Mögliche Ursachen

Der [**Flush-Aufruf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) kann aus einem von zwei Gründen fehlschlagen. Möglicherweise tritt ein Fehler auf, weil die Methode außerhalb des BeginDraw-EndDraw-Aufrufs aufgerufen wurde, oder weil ein [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Fehler von einem der Renderzielvorgänge erzeugt wurde, die seit dem letzten **Flush-Aufruf** oder **EndDraw-Aufruf** verarbeitet wurden. Um das Problem zu beheben, sollte die Anwendung die Ursache des Fehlers ermitteln und die entsprechende Aktion ergreifen.

## <a name="fixes"></a>Fehlerbehebungen

Es gibt viele Gründe, warum ein [**Flush-Aufruf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) fehlschlagen kann. Die Anwendung sollte die Ursache des Fehlers ermitteln und die entsprechende Aktion ergreifen.

 

 