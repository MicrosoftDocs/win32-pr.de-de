---
title: ID2D1Geometry Gliederungs Methoden
description: Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein ID2D1SimplifiedGeometrySink-.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Gliederungs Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372605"
---
# <a name="id2d1geometryoutline-methods"></a>ID2D1Geometry:: Outline-Methoden

Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)-.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                          | BESCHREIBUNG                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Umriss (D2D1 \_ Matrix \_ 3x2 \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)-. <br/> |
| [**Umriss (D2D1 \_ Matrix \_ 3x2 \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)-.<br/>  |
| [**Umriss (D2D1 \_ Matrix \_ 3x2 \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)-.<br/>  |
| [**Umriss (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Berechnet den Umriss der Geometrie und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)-.<br/>  |



## <a name="remarks"></a>Bemerkungen

Die Gliederungs [**Methode ermöglicht dem**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) Aufrufer das Entwickeln einer Geometrie mit einer äquivalenten Füllung für die Eingabe Geometrie mit den folgenden zusätzlichen Eigenschaften:

-   Die Ausgabe Geometrie enthält keine Querschnitte. Das heißt, Segmente können sich berühren, aber nie überschreiten.
-   Die äußersten Zahlen in der Ausgabe Geometrie werden gegen den Uhrzeigersinn ausgerichtet.
-   Die Ausgabe Geometrie ist invariant im Füllmodus. Das heißt, die Füllung der Geometrie hängt nicht von der Auswahl des Füll Modus ab. Weitere Informationen zum Füll Modus finden Sie unter [**D2D1 \_ Fill \_ Mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Außerdem kann die Gliederungs [**Methode nützlich**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) sein, um redundante Teile der genannten Geometrien zu entfernen, um komplexe Geometrien zu vereinfachen. Sie kann auch in Kombination mit [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) nützlich sein, um gleichzeitig Unions zwischen mehreren Geometrien zu erstellen.

## <a name="examples"></a>Beispiele

Der folgende Code zeigt, **wie Sie mit** Gliederung eine äquivalente Geometrie ohne selbst Austausch Vorgänge erstellen. Sie verwendet die standardmäßige Vereinfachungs Toleranz und sollte daher nicht mit sehr kleinen Geometrien verwendet werden.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

