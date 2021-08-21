---
title: gluNextContour-Funktion (Glu.h)
description: Die funktion gluNextContour markiert den Anfang einer anderen Kontur.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour-Funktion OpenGL
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
ms.openlocfilehash: 4607fbeea8e8aa46b365204bf1853c392c1a38f5ded594d840c6e9eea063da2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061598"
---
# <a name="glunextcontour-function"></a>gluNextContour-Funktion

\[Die **funktion gluNextContour** ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt. Die **funktion gluNextContour** wird [**gluTessEndContour**](glutessendcontour.md) gefolgt von [**gluTessBeginContour**](glutessbegincontour.md)zugeordnet.\]

Die **funktion gluNextContour** markiert den Anfang einer anderen Kontur.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Kontur, die definiert wird. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**GLU \_ EXTERIOR**</dt> </dl>           | Eine äußere Kontur definiert eine äußere Grenze des Polygons.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**GLU \_ INTERIOR**</dt> </dl>           | Eine innere Kontur definiert eine innere Grenze des Polygons (z. B. eine Lücke).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ UNKNOWN**</dt> </dl>              | Eine unbekannte Kontur wird von der Bibliothek analysiert, um zu bestimmen, ob es sich um ein inneres oder äußeres Erscheinungsbild handelt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, GLU \_ CW**</dt> </dl> | Die erste definierte GLU \_ CCW- oder GLU \_ CW-Kontur gilt als außen. Alle anderen Konturen werden als außen betrachtet, wenn sie in der gleichen Richtung (im Uhrzeigersinn oder gegen den Uhrzeigersinn) wie die erste Kontur ausgerichtet sind, und inner, wenn sie dies nicht sind.<br/> Wenn eine Kontur vom Typ GLU \_ CCW oder GLU \_ CW ist, müssen alle Konturen vom gleichen Typ sein (wenn dies nicht dere ist, werden alle GLU \_ CCW- und GLU \_ CW-Konturen in GLU \_ UNKNOWN geändert). Beachten Sie, dass es keinen echten Unterschied zwischen den GLU \_ CCW- und GLU \_ CW-Konturtypen gibt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **funktion gluNextContour,** um Polygone mit mehreren Konturen zu beschreiben. Nachdem Sie die erste Kontur durch eine Reihe von [**gluTessVertex-Aufrufen**](glutessvertex.md) beschrieben haben, gibt ein **gluNextContour-Aufruf** an, dass die vorherige Kontur abgeschlossen ist und dass die nächste Kontur gerade beginnt. Führen Sie eine weitere Reihe von **gluTessVertex-Aufrufen** aus, um die neue Kontur zu beschreiben. Wiederholen Sie diesen Vorgang, bis alle Konturen beschrieben wurden.

Der *Typparameter* definiert, welcher Typ von Kontur folgt.

Um den Typ der ersten Kontur zu definieren, können Sie **gluNextContour** aufrufen, bevor Sie die erste Kontur beschreiben. Wenn Sie **gluNextContour** nicht vor der ersten Kontur aufrufen, wird die erste Kontur mit GLU \_ EXTERIOR gekennzeichnet.

## <a name="examples"></a>Beispiele

Sie können ein Quadernatral mit einem dreieckigen Löcher darin wie folgt beschreiben:

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





