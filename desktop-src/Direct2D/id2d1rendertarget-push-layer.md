---
title: ID2D1RenderTarget PushLayer-Methoden (D2d1 \_ 1.h)
description: Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis PopLayer aufgerufen wird.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- PushLayer-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e1f4f5ddeace0144f6314ee7eae8a640e489d99c43f4e21f6e6c260fd003dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874030"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget::P ushLayer-Methoden

Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                            | BESCHREIBUNG                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer(D2D1 \_ LAYER \_ PARAMETERS&,ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. <br/> |
| [**PushLayer(D2D1 \_ LAYER PARAMETERS , \_ \* ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. <br/> |



## <a name="remarks"></a>Hinweise

Die [**PushLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) ermöglicht einem Aufrufer, mit dem Umleiten des Renderings auf eine Ebene zu beginnen. Alle Renderingvorgänge sind in einer Ebene gültig. Die Position der Ebene wird durch den weltweiten Transformationssatz auf dem Renderziel beeinflusst.

Jeder **PushLayer** muss über einen entsprechenden [**PopLayer-Aufruf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) verfügen. Wenn mehr **PopLayer-Aufrufe** als **PushLayer-Aufrufe** vorhanden sind, wird das Renderziel in einen Fehlerzustand versetzt. Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufgerufen wird, bevor alle ausstehenden Ebenen abgelegt werden, wird das Renderziel in einen Fehlerzustand versetzt, und es wird ein Fehler zurückgegeben. Der Fehlerzustand kann durch einen Aufruf von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)gelöscht werden.

Eine bestimmte [**ID2D1Layer-Ressource**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) kann nur gleichzeitig aktiv sein. Anders ausgedrückt: Sie können keine [**PushLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) aufrufen und dann sofort mit einer anderen **PushLayer-Methode** mit derselben Ebenenressource folgen. Stattdessen müssen Sie die zweite **PushLayer-Methode** mit unterschiedlichen Ebenenressourcen aufrufen.

Ein Beispiel finden Sie unter [Beschneiden eines Bereichs mit Ebenen.](how-to-clip-with-layers.md)

Diese Methode gibt bei einem Fehler keinen Fehlercode zurück. Überprüfen Sie das ergebnis, das von den Methoden [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wird, um zu ermitteln, ob bei einem Zeichnungsvorgang (z. B. **PushLayer)** ein Fehler aufgetreten ist.

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
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Übersicht über Ebenen](direct2d-layers-overview.md)
</dt> </dl>

�

�
