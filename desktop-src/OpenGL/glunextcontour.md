---
title: glunextcontour-Funktion (glu. h)
description: Die Funktion "glunextcontour" markiert den Anfang einer anderen Kontur.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- glunextcontour-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391708"
---
# <a name="glunextcontour-function"></a>glunextcontour-Funktion

\[Die Funktion " **glunextcontour** " ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Die **glunextcontour** -Funktion wird " [**gluTessEndContour**](glutessendcontour.md) " gefolgt von " [**glutess begincontour**](glutessbegincontour.md)" zugeordnet.\]

Die Funktion " **glunextcontour** " markiert den Anfang einer anderen Kontur.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der zu definierenden Kontur. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**Glu, \_ außen**</dt> </dl>           | Eine äußere Kontur definiert eine äußere Grenze des Polygons.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**Glu- \_ innen**</dt> </dl>           | Eine innere Kontur definiert eine innere Grenze des Polygons (z. b. eine Lücke).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**Glu \_ unbekannt**</dt> </dl>              | Eine unbekannte Kontur wird von der Bibliothek analysiert, um zu bestimmen, ob Sie innen oder außen ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**Glu \_ CCW, Glu \_ CW**</dt> </dl> | Der erste \_ definierte glu CCW-oder glu \_ CW-Contour wird als extern betrachtet. Alle anderen Konturen werden als außen betrachtet, wenn Sie in der gleichen Richtung (im Uhrzeigersinn oder gegen den Uhrzeigersinn) als erste Kontur ausgerichtet sind, und inneren, wenn dies nicht der Fall ist.<br/> Wenn eine Kontur vom Typ "glu \_ CCW" oder "glu CW" ist \_ , müssen alle Konturen denselben Typ aufweisen (wenn Sie nicht sind, werden alle \_ die Kontur CCW-und glu CW-Kontur \_ in "glu unknown" geändert \_ ). Beachten Sie, dass es keinen wirklichen Unterschied zwischen den \_ Kontur Typen glu CCW und glu \_ CW gibt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktion " **glunextcontour** ", um Polygone mit mehreren Kontur zu beschreiben. Nachdem Sie die erste Kontur durch eine Reihe von " [**glutess Vertex**](glutessvertex.md) "-aufrufen beschrieben haben, gibt ein **glunextcontour** -Aufruf an, dass die vorherige Kontur fertig ist und dass die nächste Kontur im Begriff ist, zu beginnen. Führen Sie eine weitere Reihe von **glutess Vertex** -aufrufen aus, um die neue Kontur zu beschreiben. Wiederholen Sie diesen Vorgang, bis alle Konturen beschrieben wurden.

Der *Typparameter* definiert, welcher Typ von Kontur folgt.

Um den Typ der ersten Kontur zu definieren, können Sie " **glunextcontour** " vor der Beschreibung der ersten Kontur abrufen. Wenn Sie " **glunextcontour** " nicht vor der ersten Kontur aufzurufen, wird die erste Kontur als "glu outside" gekennzeichnet \_ .

## <a name="examples"></a>Beispiele

Sie können ein Viereck mit einer dreieckigen Lücke wie folgt beschreiben:

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

[**glutess begincontour**](glutessbegincontour.md)
</dt> <dt>

[**glutess beginpolygon**](glubeginpolygon.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**glutess Vertex**](glutessvertex.md)
</dt> </dl>

 

 





