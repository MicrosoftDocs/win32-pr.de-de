---
title: ID2D1Geometry Outline-Methoden
description: Berechnet die Kontur der Geometrie und schreibt das Ergebnis in id2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Konturmethoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 3c10a777d33e0a8c9a9fa033ca2615ce2d45b2badd292757e90f88074e131549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917910"
---
# <a name="id2d1geometryoutline-methods"></a>ID2D1Geometry::Outline-Methoden

Berechnet die Kontur der Geometrie und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                          | Beschreibung                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Berechnet die Kontur der Geometrie und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). <br/> |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F \* ,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Berechnet die Kontur der Geometrie und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Berechnet die Kontur der Geometrie und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F \* ,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Berechnet die Kontur der Geometrie und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |



## <a name="remarks"></a>Hinweise

Mit [**der Outline-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) kann der Aufrufer eine Geometrie mit einer entsprechenden Füllung der Eingabegeometrie mit den folgenden zusätzlichen Eigenschaften erzeugen:

-   Die Ausgabegeometrie enthält keine Transverse-Schnittmengen. Das heißt, Segmente können sich berühren, aber nie kreuzen.
-   Die äußersten Abbildungen in der Ausgabegeometrie sind alle gegen den Uhrzeigersinn ausgerichtet.
-   Die Ausgabegeometrie ist invarianter Füllmodus. Das heißt, die Füllung der Geometrie hängt nicht von der Auswahl des Füllmodus ab. Weitere Informationen zum Füllmodus finden Sie unter [**D2D1 \_ FILL \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Darüber hinaus kann die [**Outline-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) nützlich sein, um redundante Teile der genannten Geometrien zu entfernen, um komplexe Geometrien zu vereinfachen. Es kann auch in Kombination mit [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) nützlich sein, unions zwischen mehreren Geometrien gleichzeitig zu erstellen.

## <a name="examples"></a>Beispiele

Der folgende Code zeigt, wie Sie **mithilfe** von Outline eine äquivalente Geometrie ohne Selbstschnitte erstellen. Sie verwendet die standardmäßige Vereinfachungstoleranz und sollte daher nicht mit sehr kleinen Geometrien verwendet werden.


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
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

