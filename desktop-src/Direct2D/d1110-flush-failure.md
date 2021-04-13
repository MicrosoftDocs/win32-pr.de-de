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
# <a name="d1110-flush-failure"></a>D1110: Fehler beim leeren.

Ein Flush-Befehl von einer fehlerhaften Renderziel \[ *Ressource* \] . Tags \[ *Tag1*, *Tag2* \] .

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse des Renderziels.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*Tag1*
</dt> <dd>

Der erste Tagwert. Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*Tag2*
</dt> <dd>

Der zweite Tagwert. Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> </dl> 

|             |         |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="examples"></a>Beispiele

**Beispiel 1:** Der folgende Code zeigt, dass sich ein Draw-Befehl in einem ungültigen Zustand befindet. Um die Warnmeldung zu vermeiden, verwenden Sie [**setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , um den D2D1 \_ Antialias \_ Modus- \_ Antialiasing vor einem [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Befehl festzulegen.


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





Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Beispiel 2:** Der folgende Code zeigt, dass das leeren nach dem [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Aufruf [**aufgerufen wird.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Mögliche Ursachen

Der [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) -Befehl kann aus zwei Gründen fehlschlagen. Möglicherweise tritt ein Fehler auf, weil die Methode außerhalb des [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)- / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Aufrufs aufgerufen wurde, oder es kann zu einem Fehler kommen, weil ein Fehler von einem der renderzielvorgänge  verursacht wurde, die seit dem letzten Löschvorgang oder **EndDraw** -Aufruf verarbeitet wurden. Um das Problem zu beheben, sollte die Anwendung die Ursache des Fehlers ermitteln und die entsprechende Aktion durchführen.

## <a name="fixes"></a>Fehlerbehebungen

Es gibt viele Gründe, warum ein [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) -Befehl fehlschlagen kann. Die Anwendung sollte die Ursache des Fehlers ermitteln und die entsprechende Aktion durchführen.

 

 