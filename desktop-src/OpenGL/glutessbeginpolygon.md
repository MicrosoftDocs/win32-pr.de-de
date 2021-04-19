---
title: glutess beginpolygon-Funktion (glu. h)
description: Die Funktionen "glutess beginpolygon" und "glutessendpolygon" begrenzen eine Polygon Beschreibung. | glutess beginpolygon-Funktion (glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- glutess beginpolygon-Funktion OpenGL
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
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353319"
---
# <a name="glutessbeginpolygon-function"></a>glutess beginpolygon-Funktion

Die Funktionen " **glutess beginpolygon** " und " [**glutessendpolygon**](glutessendpolygon.md) " begrenzen eine Polygon Beschreibung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*Polygon \_ Daten* 
</dt> <dd>

Ein Zeiger auf eine vom Programmierer definierte Polygon-Datenstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktionen " **glutess beginpolygon** " und " [**glutessendpolygon**](glutessendpolygon.md) " begrenzen die Definition eines nicht konvexen Polygons. Fügen Sie in jedem " **glutess beginpolygon**"-  /  Paar "glutessendpolygon" einen oder mehrere Aufrufe von " [**glutess begincontour**](glutessbegincontour.md)" ein. In jeder Kontur gibt es keine oder mehrere Aufrufe von " [**glutess Vertex**](glutessvertex.md)". Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft).

Der *Polygon- \_ Daten* Parameter ist ein Zeiger auf eine vom Programmierer definierte Datenstruktur. Wenn die entsprechenden Rückrufe angegeben werden (siehe [*glutesscallback*](glutess.md)), wird dieser Zeiger an die Rückruffunktion oder Funktionen zurückgegeben, sodass er eine bequeme Möglichkeit zum Speichern von pro-Polygon-Informationen ist.

Wenn Sie " [**glutessendpolygon**](glutessendpolygon.md)" aufrufen, wird das Polygon im Mosaik Prozess dargestellt, und die resultierenden Dreiecke werden durch Rückrufe beschrieben. Beschreibungen der Rückruf Funktionen finden Sie unter [*glutesscallback*](glutess.md).

## <a name="examples"></a>Beispiele

Im folgenden wird ein Viereck mit einer dreieckigen Lücke beschrieben:

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
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glutess begincontour**](glutessbegincontour.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**glutess normal**](glutessnormal.md)
</dt> <dt>

[**glutessproperty**](glutessproperty.md)
</dt> <dt>

[**glutess Vertex**](glutessvertex.md)
</dt> </dl>

 

 





