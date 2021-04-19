---
title: ID2D1RenderTarget-Methoden für die Methode "kreategradientstopcollection" (D2d1 \_ 1. h)
description: Erstellt ein ID2D1GradientStopCollection-Array aus dem angegebenen Array von D2D1- \_ Farbverlaufs- \_ halte Strukturen.
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4a298414d1a84b03d81c80e308113d8731369040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373671"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>ID2D1RenderTarget:: kreategradientstopcollection-Methoden

Erstellt ein [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Array aus dem angegebenen Array von [**D2D1- \_ Farbverlaufs- \_ halte**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) Strukturen.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreategradientstopcollection" (D2D1 \_ Gradient \_ Stop \* , D2D1 \_ Gamma, D2D1 \_ Extend \_ Mode, ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx) | Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus den angegebenen Farbverlaufs Stopps, dem Farb Interpolations Gamma und dem Erweiterungs Modus. <br/>                                                              |
| [**"Kreategradientstopcollection" (D2D1 \_ Gradient \_ Stop \* , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)                                                            | Erstellt ein [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Zeichen aus den angegebenen Farbverlaufs Stopps, das das [**D2D1 \_ Gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) -Farb Interpolations Gamma und den Modus für die Klammer Erweiterung verwendet.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Array von Farbverlaufs Stopps erstellt und dann verwendet, um eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)zu erstellen.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Im nächsten Codebeispiel wird [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) verwendet, um eine [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)-Datei zu erstellen.


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (Include D2d1. h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**D2D1 \_ Gradient- \_ Stopps**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Erstellen eines linearen Farbverlaufs Pinsels](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Erstellen eines radialen Farbverlaufs Pinsels](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>
