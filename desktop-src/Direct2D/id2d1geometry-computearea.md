---
title: ID2D1Geometry computearea-Methoden
description: Berechnet den Bereich der Geometrie.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Computearea-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358801"
---
# <a name="id2d1geometrycomputearea-methods"></a>ID2D1Geometry:: computearea-Methoden

Berechnet den Bereich der Geometrie.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                      | BESCHREIBUNG                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der Standardtoleranz vereinfacht wurde.<br/>    |
| [**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der Standardtoleranz vereinfacht wurde.<br/> |
| [**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.<br/>  |
| [**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.<br/>  |



## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **computearea** verwendet, um den Bereich eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
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

 

