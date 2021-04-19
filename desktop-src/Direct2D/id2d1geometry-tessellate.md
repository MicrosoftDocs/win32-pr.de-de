---
title: ID2D1Geometry-Mosaik Methoden
description: Erstellt einen Satz von Dreiecken in Uhrzeigerrichtung, die die Geometrie abdecken, nachdem sie mit der angegebenen Matrix transformiert und mit der angebenen Toleranz vereinfacht wurde.
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Mosaik Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 060fc42dddd7642f021d073b8addbe089d031393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367687"
---
# <a name="id2d1geometrytessellate-methods"></a>ID2D1Geometry:: Mosaik-Methoden

Erstellt einen Satz von Dreiecken in Uhrzeigerrichtung, die die Geometrie abdecken, nachdem sie mit der angegebenen Matrix transformiert und mit der angebenen Toleranz vereinfacht wurde.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mosaik (D2D1 \_ Matrix \_ 3x2 \_ F \* , ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | Erstellt eine Reihe von Dreiecken im Uhrzeigersinn, die die Geometrie abdecken, nachdem Sie mit der angegebenen Matrix transformiert und mit der Standardtoleranz vereinfacht wurde. <br/>   |
| [**Mosaik (D2D1 \_ Matrix \_ 3x2 \_ F&, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | Erstellt eine Reihe von Dreiecken im Uhrzeigersinn, die die Geometrie abdecken, nachdem Sie mit der angegebenen Matrix transformiert und mit der Standardtoleranz vereinfacht wurde. <br/>   |
| [**Mosaik (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | Erstellt einen Satz von Dreiecken in Uhrzeigerrichtung, die die Geometrie abdecken, nachdem sie mit der angegebenen Matrix transformiert und mit der angebenen Toleranz vereinfacht wurde. <br/> |
| [**Mosaik (D2D1 \_ Matrix \_ 3x2 \_ F&, float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | Erstellt einen Satz von Dreiecken in Uhrzeigerrichtung, die die Geometrie abdecken, nachdem sie mit der angegebenen Matrix transformiert und mit der angebenen Toleranz vereinfacht wurde.<br/>  |



## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie Sie mithilfe von "Mosaik" eine Reihe von Dreiecken im Uhrzeigersinn erstellen, die die Geometrie abdecken.


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
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

