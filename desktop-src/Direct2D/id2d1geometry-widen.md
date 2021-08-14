---
title: ID2D1Geometry Widen-Methoden
description: Breitet die Geometrie um den angegebenen Strich und schreibt das Ergebnis in eine ID2D1SimplifiedGeometrySink.
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- Widen-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: ebdae7ba4fd9eca96e422ae62274b4b9934040d4c4249bc9e1c78b81b62589dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342810"
---
# <a name="id2d1geometrywiden-methods"></a>ID2D1Geometry::Widen-Methoden

Breitet die Geometrie um den angegebenen Strich und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F \* ,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))             | Breitet die Geometrie um den angegebenen Strich und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) nachdem sie von der angegebenen Matrix transformiert und mithilfe der Standardtoleranz vereinfacht wurde.<br/>   |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))              | Breitet die Geometrie um den angegebenen Strich und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) nachdem sie von der angegebenen Matrix transformiert und mithilfe der Standardtoleranz vereinfacht wurde.<br/>   |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F \* ,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Breitet die Geometrie um den angegebenen Strich aus und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) nachdem sie von der angegebenen Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.<br/> |
| [**Widen(FLOAT,ID2D1StrokeStyle \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))  | Breitet die Geometrie um den angegebenen Strich aus und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) nachdem sie von der angegebenen Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.<br/> |



## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie **Widen** verwendet wird, um die Geometrie um den angegebenen Strich zu verbreitern und das Ergebnis dann in ein [**ID2D1SimplifiedGeometrySink-Objekt zu**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) schreiben.


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
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

 

