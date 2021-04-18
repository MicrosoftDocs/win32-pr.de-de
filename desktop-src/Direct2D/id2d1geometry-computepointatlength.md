---
title: ID2D1Geometry computepointatlength-Methoden
description: Berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der \ 160; Geometrie.
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- Computepointatlength-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5b49be0b5a17dd828c9bd86ca41b4a3ff115f47a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365411"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>ID2D1Geometry:: computepointatlength-Methoden

Berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der Geometrie.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Computepointatlength (float, D2D1 \_ Matrix \_ 3x2 \_ F&, D2D1 \_ Point \_ 2f \* , D2D1 \_ Point \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | Berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der Standardtoleranz vereinfacht wurde.<br/>   |
| [**Computepointatlength (float, D2D1 \_ Matrix \_ 3x2 \_ F \* , D2D1 \_ Point \_ 2f \* , D2D1 \_ Point \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | Berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der Standardtoleranz vereinfacht wurde.<br/>   |
| [**Computepointatlength (float, D2D1 \_ Matrix \_ 3x2 \_ F&, float, D2D1 \_ Point \_ 2f \* , D2D1 \_ Point \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | Berechnet den Punkt und den Tangenten Vektor im angegebenen Abstand entlang der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der angegebenen Toleranz vereinfacht wurde.<br/> |
| [**Computepointatlength (float, D2D1 \_ Matrix \_ 3x2 \_ F \* , float, D2D1 \_ Point \_ 2f \* , D2D1 \_ Point \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | Berechnet den Punkt und den Tangenten Vektor im angegebenen Abstand entlang der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der angegebenen Toleranz vereinfacht wurde.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie mit **computepointatlength** der Punkt und der Tangens Vektor in der angegebenen Entfernung entlang der Geometrie berechnet werden.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
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

 

