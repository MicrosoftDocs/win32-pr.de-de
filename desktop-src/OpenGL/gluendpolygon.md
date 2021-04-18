---
title: gluendpolygon-Funktion (glu. h)
description: Die Funktionen "glubeginpolygon" und "gluendpolygon" begrenzen eine Polygon Beschreibung. | gluendpolygon-Funktion (glu. h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- gluendpolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351874"
---
# <a name="gluendpolygon-function"></a>gluendpolygon-Funktion

\[Die Funktion " **gluendpolygon** " ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Die Funktion " **gluendpolygon** " ist " **glutessendpolygon** " gefolgt von " **gluTessEndContour**" zugeordnet.\]

Die Funktionen " [**glubeginpolygon**](glubeginpolygon.md) " und " **gluendpolygon** " begrenzen eine Polygon Beschreibung.

## <a name="syntax"></a>Syntax


```C++
void gluEndPolygon(
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

Verwenden Sie " [**glubeginpolygon**](glubeginpolygon.md) " und " **gluendpolygon** ", um die Definition eines nicht konvexen Polygons zu begrenzen.

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

 

 





