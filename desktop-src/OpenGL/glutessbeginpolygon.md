---
title: gluTessBeginPolygon-Funktion (Glu.h)
description: Die Funktionen gluTessBeginPolygon und gluTessEndPolygon begrenzen eine Polygonbeschreibung. | gluTessBeginPolygon-Funktion (Glu.h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42566cf8a0674086883e6333a67ac2df03329f6a9bd3bb903ef558af3c430b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777390"
---
# <a name="glutessbeginpolygon-function"></a>gluTessBeginPolygon-Funktion

Die **Funktionen gluTessBeginPolygon** und [**gluTessEndPolygon**](glutessendpolygon.md) begrenzen eine Polygonbeschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*\_Polygondaten* 
</dt> <dd>

Ein Zeiger auf eine vom Programmierer definierte Polygondatenstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **Funktionen gluTessBeginPolygon** und [**gluTessEndPolygon**](glutessendpolygon.md) begrenzen die Definition eines nicht konvexen Polygons. Schließen Sie **in jedem gluTessBeginPolygon-gluTessEndPolygon-Paar** mindestens einen Aufruf von  /   [**gluTessBeginContour ein.**](glutessbegincontour.md) Innerhalb jeder Kontur gibt es null oder mehr Aufrufe von [**gluTessVertex**](glutessvertex.md). Die Scheitelpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit der ersten kontur verknüpft).

Der *\_ Polygondatenparameter* ist ein Zeiger auf eine vom Programmierer definierte Datenstruktur. Wenn die entsprechenden Rückrufe angegeben werden (siehe [*gluTessCallback),*](glutess.md)wird dieser Zeiger an die Rückruffunktion bzw. die Rückruffunktionen zurückgegeben, was eine praktische Möglichkeit zum Speichern von Informationen pro Polygon ist.

Wenn Sie [**gluTessEndPolygon**](glutessendpolygon.md)aufrufen, wird das Polygon mosaikiert, und die resultierenden Dreiecke werden durch Rückrufe beschrieben. Beschreibungen der Rückruffunktionen finden Sie unter [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Beispiele

Im Folgenden wird eine quadräre Lücke mit einer dreieckigen Lücke beschrieben:

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





