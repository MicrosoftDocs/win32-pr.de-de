---
title: gluBeginPolygon-Funktion (Glu.h)
description: Die Funktionen gluBeginPolygon und gluEndPolygon begrenzen eine Polygonbeschreibung. | gluBeginPolygon-Funktion (Glu.h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- gluBeginPolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98fe58a48a10d36a07e3a96bdfe612d8857f691233e19faac670eb6d987b42f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937893"
---
# <a name="glubeginpolygon-function"></a>gluBeginPolygon-Funktion

\[Die **funktion gluBeginPolygon** ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Die **gluBeginPolygon-Funktion** wird [**gluTessBeginPolygon**](glutessbeginpolygon.md) gefolgt von [**gluTessBeginContour**](glutessbegincontour.md)zugeordnet.\]

Die Funktionen **gluBeginPolygon** und [**gluEndPolygon**](gluendpolygon.md) begrenzen eine Polygonbeschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluBeginPolygon** und **gluEndPolygon,** um die Definition eines Nichtkonvexpolygons zu begrenzen.

1.  Rufen Sie **gluBeginPolygon** auf.
2.  Definieren Sie die Konturen des Polygons, indem [**Sie gluTessVertex**](glutessvertex.md) für jeden Scheitelpunkt und [**gluNextContour**](glunextcontour.md) aufrufen, um jede neue Kontur zu starten.
3.  Rufen Sie **gluEndPolygon** auf, um das Ende der Definition zu signalisieren.

    Sobald **gluEndPolygon** aufgerufen wird, wird das Polygon mosaikiert, und die resultierenden Dreiecke werden durch Rückrufe beschrieben. Beschreibungen der Rückruffunktionen finden Sie unter [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Quadernatral mit einer dreieckigen Lücke beschrieben:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





