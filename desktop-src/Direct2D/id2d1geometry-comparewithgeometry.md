---
title: ID2D1Geometry comparewithgeometry-Methoden
description: Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Comparewithgeometry-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eee64e51d4717a9fe0983be849c78f99602cac9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374022"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>ID2D1Geometry:: comparewithgeometry-Methoden

Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comparewithgeometry (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3x2 \_ F&, D2D1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der standardmäßigen Vereinfachungs Toleranz.<br/>      |
| [**Comparewithgeometry (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3x2 \_ F \* , D2D1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der standardmäßigen Vereinfachungs Toleranz.<br/>      |
| [**Comparewithgeometry (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3x2 \_ F&, float, D2D1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der angegebenen Vereinfachungs Toleranz.<br/>    |
| [**Comparewithgeometry (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3x2 \_ F \* , float, D2D1 \_ Geometry \_ Relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Beschreibt die Schnittmenge zwischen dieser Geometrie und der angegebenen Geometrie. Der Vergleich erfolgt mithilfe der angegebenen Vereinfachungs Toleranz.<br/> |



## <a name="remarks"></a>Bemerkungen

Beachten Sie beim Interpretieren des zurückgegebenen *Beziehungs* Werts, dass der Member D2D1 Geometry-Beziehung im Enumerationstyp **D2D1 \_ Geometry- \_ Beziehung** [**\_ \_ \_ \_ enthalten ist**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) , dass diese Geometrie in *inputgeometry* enthalten ist, nicht dass diese Geometrie *inputgeometry* enthält.

Weitere Informationen zum Interpretieren anderer möglicher Rückgabewerte finden Sie unter [**D2D1 \_ Geometry \_ Relation**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

