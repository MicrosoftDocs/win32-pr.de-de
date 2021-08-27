---
title: ID2D1RenderTarget CreateLayer-Methoden (D2d1.h)
description: Erstellt eine Ebenenressource, die mit diesem Renderziel und den kompatiblen Renderzielen verwendet werden kann.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- CreateLayer-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a351c9e1b4fc36c816e87aeaae79a591bb43768a4e098bf315990fc1e1794fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131490"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a>ID2D1RenderTarget::CreateLayer-Methoden

Erstellt eine Ebenenressource, die mit diesem Renderziel und den kompatiblen Renderzielen verwendet werden kann.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                 | Beschreibung                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLayer(ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Erstellt eine Ebenenressource, die mit diesem Renderziel und den kompatiblen Renderzielen verwendet werden kann. <br/>                                               |
| [**CreateLayer(D2D1 \_ SIZE \_ F,ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Erstellt eine Ebenenressource, die mit diesem Renderziel und den kompatiblen Renderzielen verwendet werden kann. Die neue Ebene hat die angegebene Anfangsgröße. <br/> |
| [**CreateLayer(D2D1 \_ SIZE F , \_ \* ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Erstellt eine Ebenenressource, die mit diesem Renderziel und den kompatiblen Renderzielen verwendet werden kann. Die neue Ebene hat die angegebene Anfangsgröße. <br/> |



## <a name="remarks"></a>Hinweise

Die Größe der Ebene wird bei Bedarf automatisch selbst geändert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Ebene verwendet, um eine Bitmap auf eine geometrische Maske zu beschneiden. Das vollständige Beispiel finden Sie unter [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).


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
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Ebenen](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
