---
title: ID2D1RenderTarget CreateGradientStopCollection-Methoden (D2d1 \_ 1.h)
description: Erstellt eine ID2D1GradientStopCollection aus dem angegebenen Array von D2D1 \_ GRADIENT \_ STOP-Strukturen.
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- CreateGradientStopCollection-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e149727650223f40a290d1ada40abc69f9033440
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380634"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>ID2D1RenderTarget::CreateGradientStopCollection-Methoden

Erstellt eine [**ID2D1GradientStopCollection aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) dem angegebenen Array von [**D2D1 \_ GRADIENT \_ STOP-Strukturen.**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                               | Beschreibung                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,D2D1 \_ GAMMA,D2D1 \_ EXTEND \_ MODE,ID2D1GradientStopCollection \* \* )**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx) | Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus den angegebenen Farbverlaufsstopps, Farbinterpolation gamma und dem angegebenen Erweiterungsmodus. <br/>                                                              |
| [**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,ID2D1GradientStopCollection \* \* )**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)                                                            | Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus den angegebenen Farbverlaufsstopps, die die Farbinterpolation [**D2D1 \_ GAMMA \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) und den Klammerdehnungsmodus verwendet.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Array von Farbverlaufsstopps erstellt und anschließend verwendet, um eine [**ID2D1GradientStopCollection zu erstellen.**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)


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



Im nächsten Codebeispiel wird [**id2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) verwendet, um einen [**ID2D1LinearGradientBrush zu erstellen.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)


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
| Header<br/>  | <dl> <dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**D2D1 \_ GRADIENT \_ STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Erstellen eines Pinsels mit linearem Farbverlauf](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Erstellen eines Pinsels mit radialem Farbverlauf](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>
