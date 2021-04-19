---
title: glubeginpolygon-Funktion (glu. h)
description: Die Funktionen "glubeginpolygon" und "gluendpolygon" begrenzen eine Polygon Beschreibung. | glubeginpolygon-Funktion (glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- glubeginpolygon-Funktion OpenGL
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
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355755"
---
# <a name="glubeginpolygon-function"></a>glubeginpolygon-Funktion

\[Die Funktion " **glubeginpolygon** " ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Die Funktion " **glubeginpolygon** " ist " [**glutess beginpolygon**](glutessbeginpolygon.md) " gefolgt von " [**glutess begincontour**](glutessbegincontour.md)" zugeordnet.\]

Die Funktionen " **glubeginpolygon** " und " [**gluendpolygon**](gluendpolygon.md) " begrenzen eine Polygon Beschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glubeginpolygon** " und " **gluendpolygon** ", um die Definition eines nicht konvexen Polygons zu begrenzen.

1.  Aufrufen von " **glubeginpolygon**".
2.  Definieren Sie die Kontur des Polygons, indem Sie für jeden Scheitelpunkt und [**glunextcontour**](glunextcontour.md) den Wert " [**glutess Vertex**](glutessvertex.md) " aufrufen, um die einzelnen neuen Konturen zu starten
3.  Nennen Sie " **gluendpolygon** ", um das Ende der Definition zu signalisieren.

    Nachdem " **gluendpolygon** " aufgerufen wurde, wird das Polygon im Mosaik Prozess dargestellt, und die resultierenden Dreiecke werden durch Rückrufe beschrieben. Beschreibungen der Rückruf Funktionen finden Sie unter [*glutesscallback*](glutess.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Viereck mit einer dreieckigen Lücke beschrieben:

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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glunextcontour**](glunextcontour.md)
</dt> <dt>

[**glutess begincontour**](glutessbegincontour.md)
</dt> <dt>

[**glutess beginpolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> <dt>

[**glutess Vertex**](glutessvertex.md)
</dt> </dl>

 

 





