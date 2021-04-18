---
title: ID2D1RenderTarget pushlayer-Methoden (D2d1 \_ 1. h)
description: Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis poplayer aufgerufen wird.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Pushlayer-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364487"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget::P ushlayer-Methoden

Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                            | BESCHREIBUNG                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pushlayer (D2D1 \_ Layer \_ Parameters&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. <br/> |
| [**Pushlayer (D2D1 \_ Layer \_ Parameters \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. <br/> |



## <a name="remarks"></a>Bemerkungen

Mithilfe der [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode kann ein Aufrufer mit dem Umleiten des Rendering zu einer Ebene beginnen. Alle Renderingvorgänge sind in einer Ebene gültig. Der Speicherort der Ebene wird von der Welt Transformation beeinflusst, die auf dem Renderziel festgelegt ist.

Jede **pushschicht** muss über einen passenden [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) -Befehl verfügen. Wenn mehr **poplayer** -Aufrufe als **pushlayer** -Aufrufe vorhanden sind, wird das Renderziel in einen Fehlerzustand versetzt. Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) vor allen ausstehenden Ebenen aufgerufen wird, wird das Renderziel in einen Fehlerzustand versetzt, und es wird ein Fehler zurückgegeben. Der Fehlerzustand kann durch einen Aufrufen von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)gelöscht werden.

Eine bestimmte [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Ressource kann nur zu einem bestimmten Zeitpunkt aktiv sein. Anders ausgedrückt: Sie können keine [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode aufzurufen und dann sofort mit einer anderen **pushlayer** -Methode mit derselben ebenenressource folgen. Stattdessen müssen Sie die zweite **pushlayer** -Methode mit unterschiedlichen ebenenressourcen abrufen.

Ein Beispiel finden Sie unter Gewusst [wie: Abschneiden eines Bereichs mit Ebenen](how-to-clip-with-layers.md).

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **pushlayer**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

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
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (Include D2d1. h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Übersicht über Schichten](direct2d-layers-overview.md)
</dt> </dl>

�

�
