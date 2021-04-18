---
title: ID2D1RenderTarget-Methoden für "kreatelayer" (D2d1. h)
description: Erstellt eine ebenenressource, die mit diesem Renderziel und den kompatiblen renderzielen verwendet werden kann.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Methoden von "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6e7fe86f041a818db77c28ed9461d8c8fb48ad64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368338"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a>ID2D1RenderTarget:: kreatelayer-Methoden

Erstellt eine ebenenressource, die mit diesem Renderziel und den kompatiblen renderzielen verwendet werden kann.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                 | BESCHREIBUNG                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"ID2D1Layer" ( \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Erstellt eine ebenenressource, die mit diesem Renderziel und den kompatiblen renderzielen verwendet werden kann. <br/>                                               |
| [**Kreatelayer (D2D1 \_ size \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Erstellt eine ebenenressource, die mit diesem Renderziel und den kompatiblen renderzielen verwendet werden kann. Die neue Ebene hat die angegebene anfangs Größe. <br/> |
| [**Kreatelayer (D2D1 \_ size \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Erstellt eine ebenenressource, die mit diesem Renderziel und den kompatiblen renderzielen verwendet werden kann. Die neue Ebene hat die angegebene anfangs Größe. <br/> |



## <a name="remarks"></a>Bemerkungen

Die Größe der Ebene wird nach Bedarf automatisch angepasst.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine-Ebene verwendet, um eine Bitmap an eine geometrische Maske auszuschneiden. Das komplette Beispiel finden Sie unter Gewusst [wie: Abschneiden einer geometrischen Maske](how-to-clip-with-layers.md).


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Schichten](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
