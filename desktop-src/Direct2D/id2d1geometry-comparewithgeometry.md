---
title: ID2D1Geometry CompareWithGeometry-Methoden
description: Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- CompareWithGeometry-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09978c38c3e4be7ad8a86ccfccb43387ed4ac48232e39e1ed19001d806362c88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304800"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>ID2D1Geometry::CompareWithGeometry-Methoden

Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der Standardabflaungstoleranz.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F \* ,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der Standardabflaungstoleranz.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der angegebenen Flatteningtoleranz.<br/>    |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F \* ,FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich wird mithilfe der angegebenen Flatteningtoleranz durchgeführt.<br/> |



## <a name="remarks"></a>Hinweise

Beachten Sie  beim Interpretieren des zurückgegebenen Beziehungswerts, dass der Member [**D2D1 \_ GEOMETRY \_ RELATION \_ IS \_ CONTAINED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) des Enumerationstyps **D2D1 \_ GEOMETRY \_ RELATION** bedeutet, dass diese Geometrie in *inputGeometry* enthalten ist, nicht, dass diese Geometrie *inputGeometry enthält.*

Weitere Informationen zum Interpretieren anderer möglicher Rückgabewerte finden Sie unter [**D2D1 \_ GEOMETRY \_ RELATION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

