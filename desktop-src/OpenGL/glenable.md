---
title: glEnable-Funktion (GL. h)
description: Die Funktionen "glEnable" und "gldeaktivieren" aktivieren oder deaktivieren OpenGL-Funktionen. | glEnable-Funktion (GL. h)
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- glEnable-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc2d13233afec956c798805295c44c96df45d04
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367325"
---
# <a name="glenable-function"></a>glEnable-Funktion

Die Funktionen " **glEnable** " und " [**gldeaktivieren**](gldisable.md) " aktivieren oder deaktivieren OpenGL-Funktionen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Decke* 
</dt> <dd>

Eine symbolische Konstante, die eine OpenGL-Funktion angibt.

Eine Erläuterung der Werte, die die *Obergrenze* annehmen kann, finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Cap* war keiner der Werte, die im vorherigen Abschnitt "Hinweise" aufgeführt sind.<br/>                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktionen " **glEnable** " und " **gldeaktivieren** " aktivieren und deaktivieren verschiedene OpenGL-Grafikfunktionen. Verwenden Sie " [**glisenabled**](glisenabled.md) " oder " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die aktuelle Einstellung einer beliebigen Funktion zu bestimmen.

Sowohl **glEnable** als auch **glEnable** verwenden ein einzelnes Argument ( *Cap*), das einen der folgenden Werte annehmen kann:



| Wert                       | Bedeutung                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL- \_ alpha \_ Test             | Wenn diese Option aktiviert ist, führen Sie Alpha Tests durch. Siehe [**glalphafunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ Auto \_ Normal            | Wenn diese Option aktiviert ist, werden normale Vektoren bei der Generierung von GL \_ map2 \_ Vertex \_ 3 oder GL \_ map2 Scheitel Punkten durch \_ Scheitel \_ Punkte analytisch berechnet. Siehe [**glMap2**](glmap2.md).                                                                                        |
| GL \_ Blend                   | Wenn diese Option aktiviert ist, werden die eingehenden RGBA-Farbwerte mit den Werten in den Farb Puffern in Blend Siehe [**glblendfunc**](glblendfunc.md).                                                                                                                              |
| GL \_ - \_ clippinbene *i*          | Wenn diese Option aktiviert ist, schneiden Sie Geometry für die benutzerdefinierte Clippingebene *i* ab. Siehe [**glclipplane**](glclipplane.md).                                                                                                                                                  |
| GL- \_ Farb \_ Logik- \_ op        | Wenn diese Option aktiviert ist, wird der aktuelle logische Vorgang auf die eingehenden RGBA-Farb-und Farb Puffer Werte angewendet. Siehe [**gllogicop**](gllogicop.md).                                                                                                                     |
| GL- \_ Farb \_ Material         | Wenn diese Option aktiviert ist, muss mindestens ein Materialparameter die aktuelle Farbe verfolgen. Siehe [**glcolormaterial**](glcolormaterial.md).                                                                                                                                   |
| GL. Ober \_ \_ Fläche              | Wenn diese Option aktiviert ist, werden Polygone auf Grundlage ihres aufwicklungs Fensters in Fenster Koordinaten angezeigt. Siehe [**glcullface**](glcullface.md).                                                                                                                                               |
| GL- \_ tiefen \_ Test             | Wenn diese Option aktiviert ist, werden tiefen Vergleiche durchführen und der tiefen Puffer aktualisiert. Weitere Informationen finden Sie unter [**gldepthfunc**](gldepthfunc.md) und [**gldepthrange**](gldepthrange.md).                                                                                                              |
| GL \_ .                  | Wenn diese Option aktiviert ist, werden Komponenten oder Indizes vor dem Schreiben in den Farb Puffer unterschieden.                                                                                                                                                                 |
| GL- \_ Nebel                     | Wenn diese Option aktiviert ist, wird eine Nebelfarbe in die Post-texturierungsfarbe umgewandelt. Siehe [**glnebel**](glfog.md).                                                                                                                                                                    |
| GL- \_ Index \_ Logik- \_ op        | Wenn diese Option aktiviert ist, wird die aktuelle logische Operation auf die eingehenden Index-und Farb Puffer Indizes angewendet. Siehe [**gllogicop**](gllogicop.md).                                                                                                                         |
| GL \_ Light *i*                | Wenn diese Option aktiviert ist, sollten Sie Light *i* in die Auswertung der Beleuchtungs Gleichung einschließen. Siehe [**gllightmodel**](gllightmodel-functions.md) und [**gllight**](gllight-functions.md).                                                                                      |
| GL- \_ Beleuchtung                | Wenn diese Option aktiviert ist, verwenden Sie die aktuellen Beleuchtungs Parameter, um die Vertexfarbe oder den Index zu berechnen. Wenn diese Option deaktiviert ist, ordnen Sie die aktuelle Farbe oder den aktuellen Index jedem Scheitelpunkt zu Siehe [**glmaterial**](glmaterial-functions.md), **gllightmodel** und **gllight**.                |
| GL- \_ Linie \_ glatt            | Wenn diese Option aktiviert ist, zeichnen Sie Linien mit korrekter Filterung. Wenn diese Option deaktiviert ist, zeichnen Sie Zeilen mit Zeilen. Siehe [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| GL- \_ Zeilen \_ Stippel           | Wenn diese Option aktiviert ist, verwenden Sie das aktuelle Zeilen stippingmuster beim Zeichnen von Linien. Siehe [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| GL- \_ Logik- \_ op               | Wenn diese Option aktiviert ist, wird der aktuell ausgewählte logische Vorgang auf die eingehenden und Farb Puffer Indizes angewendet. Siehe [**gllogicop**](gllogicop.md).                                                                                                                    |
| GL \_ zuordnung1 \_ Farbe \_ 4          | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) RGBA-Werte. Siehe auch [**glMap1**](glmap1.md).                                           |
| GL \_ zuordnung1 \_ Index             | Wenn diese Option aktiviert ist, werden bei Aufrufen von **glEvalCoord1**, **glEvalMesh1** und **glEvalPoint1** Farbindizes generiert. Siehe auch **glMap1**.                                                                                                                                   |
| GL \_ zuordnung1 \_ Normal            | Wenn diese Option aktiviert ist, werden bei Aufrufen von [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) normale generiert. Siehe auch [**glMap1**](glmap1.md).                                               |
| GL \_ zuordnung1 \_ Textur \_ Koord \_ 1 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord1**, **glEvalMesh1** und **glEvalPoint1** *s* -Texturkoordinaten. Siehe auch **glMap1**.                                                                                                                         |
| GL \_ zuordnung1 \_ Textur- \_ Koord \_ 2 | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) *s* -und *t* -Texturkoordinaten. Siehe auch [**glMap1**](glmap1.md).                       |
| GL \_ zuordnung1 \_ Textur \_ Koord \_ 3 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord1**, **glEvalMesh1** und **glEvalPoint1** die Texturkoordinaten *s*, *t* und *r* . Siehe auch **glMap1**.                                                                                                           |
| GL \_ zuordnung1 \_ Textur- \_ Koord \_ 4 | Wenn diese Option aktiviert ist, generieren Aufrufe von [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) *s*-, *t*-, *r*-und *q* -Texturkoordinaten. Siehe auch [**glMap1**](glmap1.md).                    |
| GL \_ zuordnung1 \_ Scheitelpunkt \_ 3         | Wenn diese Option aktiviert ist, werden von Aufrufen von **glEvalCoord1**, **glEvalMesh1** und **glEvalPoint1** *x*-, *y*-und *z* -Scheitelpunkt Koordinaten generiert. Siehe auch **glMap1**.                                                                                                            |
| GL \_ zuordnung1 \_ Scheitelpunkt \_ 4         | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) homogene *x*-, *y*-, *z*-und *w* -Scheitelpunkt Koordinaten. Siehe auch [**glMap1**](glmap1.md). |
| GL \_ map2 \_ Farbe \_ 4          | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) RGBA-Werte. Siehe auch [**glMap2**](glmap2.md).                                           |
| GL \_ map2 \_ Index             | Wenn diese Option aktiviert ist, werden bei Aufrufen von **glEvalCoord2**, **glEvalMesh2** und **glEvalPoint2** Farbindizes generiert. Siehe auch **glMap2**.                                                                                                                                   |
| GL \_ map2 \_ Normal            | Wenn diese Option aktiviert ist, werden bei Aufrufen von [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) normale generiert. Siehe auch [**glMap2**](glmap2.md).                                               |
| GL \_ map2 \_ Textur \_ Koord \_ 1 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2**, **glEvalMesh2** und **glEvalPoint2** *s* -Texturkoordinaten. Siehe auch **glMap2**.                                                                                                                         |
| GL \_ map2 \_ Textur- \_ Koord \_ 2 | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) *s* -und *t* -Texturkoordinaten. Siehe auch [**glMap2**](glmap2.md).                       |
| GL \_ map2 \_ Textur \_ Koord \_ 3 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2**, **glEvalMesh2** und **glEvalPoint2** die Texturkoordinaten *s*, *t* und *r* . Siehe auch **glMap2**.                                                                                                           |
| GL \_ map2 \_ Textur- \_ Koord \_ 4 | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) *s*-, *t*-, *r*-und *q* -Texturkoordinaten. Siehe auch [**glMap2**](glmap2.md).            |
| GL \_ map2 \_ Scheitelpunkt \_ 3         | Wenn diese Option aktiviert ist, werden von Aufrufen von **glEvalCoord2**, **glEvalMesh2** und **glEvalPoint2** *x*-, *y*-und *z* -Scheitelpunkt Koordinaten generiert. Siehe auch **glMap2**.                                                                                                            |
| GL \_ map2 \_ Scheitelpunkt \_ 4         | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) homogene *x*-, *y*-, *z*-und *w* -Scheitelpunkt Koordinaten. Siehe auch [**glMap2**](glmap2.md). |
| GL \_ normalize               | Wenn diese Option aktiviert ist, werden die mit **glnormal** angegebenen normalen Vektoren nach der Transformation auf die Einheiten Länge skaliert. Siehe [**glnormal**](glnormal-functions.md).                                                                                                          |
| GL- \_ Punkt \_ glatt           | Wenn diese Option aktiviert ist, zeichnen Sie Punkte mit ordnungsgemäßer Filterung. Wenn diese Option deaktiviert ist, zeichnen Sie Aliasing Punkte. Siehe [**glPointSize**](glpointsize.md).                                                                                                                                    |
| GL- \_ Polygon- \_ Offset \_ Füllung   | Wenn diese Option aktiviert ist und das Polygon im GL \_ -Füllmodus gerendert wird, wird den tiefen Werten der Fragmente eines Polygons ein Offset hinzugefügt, bevor der tiefen Vergleich durchgeführt wird. Siehe [**glpolygonoffset**](glpolygonoffset.md)**.**                                      |
| GL- \_ Polygon- \_ Offset \_ Linie   | Wenn diese Option aktiviert ist und das Polygon im GL \_ -Zeilen Modus gerendert wird, wird den tiefen Werten der Fragmente eines Polygons ein Offset hinzugefügt, bevor der tiefen Vergleich durchgeführt wird. Siehe **glpolygonoffset**.                                                                 |
| GL- \_ Polygon- \_ Offset \_ Punkt  | Wenn diese Option aktiviert ist, wird den tiefen Werten der Fragmente eines Polygons ein Offset hinzugefügt, bevor der tiefen Vergleich durchgeführt wird, wenn das Polygon im GL-Punkt Modus gerendert wird \_ . Siehe [**glpolygonoffset**](glpolygonoffset.md).                                             |
| GL- \_ Polygon \_ glatt         | Wenn diese Option aktiviert ist, zeichnen Sie Polygone mit dem richtigen Filter. Wenn diese Option deaktiviert ist, zeichnen Sie Polygone mit Alias. Siehe [**glpolygonmode**](glpolygonmode.md).                                                                                                                            |
| GL- \_ Polygon- \_ Stippel        | Wenn diese Option aktiviert ist, verwenden Sie das aktuelle Polygon Stippel Muster beim Rendern von Polygonen. Siehe [**glpolygonstippel**](glpolygonstipple.md).                                                                                                                              |
| GL- \_ Scissor- \_ Test           | Wenn diese Option aktiviert ist, verwerfen Sie Fragmente außerhalb des Scheren Rechtecks. Siehe [**glscissor**](glscissor.md).                                                                                                                                                   |
| GL- \_ Schablonen \_ Test           | Wenn diese Option aktiviert ist, führen Sie Schablonen Tests aus, und aktualisieren Sie den Schablonen Puffer. Weitere Informationen finden Sie unter [**glstencilfunc**](glstencilfunc.md) und [**glstencilop**](glstencilop.md).                                                                                                            |
| GL \_ \_ -Textur 1D             | Wenn diese Option aktiviert ist, wird eine eindimensionale Texturierung ausgeführt (es sei denn, die zweidimensionale Texturierung ist ebenfalls aktiviert). Siehe [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| GL \_ Textur \_ 2D             | Wenn diese Option aktiviert ist, wird eine zweidimensionale Texturierung ausgeführt. Siehe [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| GL \_ Textur \_ gen, \_ Q         | Wenn diese Option aktiviert ist, wird die *q* -Textur Koordinate mithilfe der Textur Generierungs Funktion berechnet, die mit [**gltexgen**](gltexgen-functions.md)definiert wurde. Andernfalls wird die aktuelle *q* -Textur Koordinate verwendet.                                                        |
| GL \_ Textur \_ gen \_ R         | Wenn diese Option aktiviert ist, wird die *r* -Textur Koordinate mithilfe der in [**gltexgen**](gltexgen-functions.md)definierten Textur Generierungs Funktion berechnet. Wenn diese Option deaktiviert ist, wird die aktuelle *r* -Textur Koordinate verwendet.                                                      |
| GL- \_ Textur \_ gen \_ S         | Wenn diese Option aktiviert ist, wird die *s* -Textur Koordinate mithilfe der in **gltexgen** definierten Textur Generierungs Funktion berechnet. Wenn diese Option deaktiviert ist, wird die aktuelle *s* -Textur Koordinate verwendet.                                                                                |
| GL \_ Textur \_ gen \_ T         | Wenn diese Option aktiviert ist, wird die *t* -Textur Koordinate mithilfe der in [**gltexgen**](gltexgen-functions.md)definierten Textur Generierungs Funktion berechnet. Wenn diese Option deaktiviert ist, wird die aktuelle *t* -Textur Koordinate verwendet.                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glalphafunc**](glalphafunc.md)
</dt> <dt>

[**glarrayelement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**glclipplane**](glclipplane.md)
</dt> <dt>

[**glcolormaterial**](glcolormaterial.md)
</dt> <dt>

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**glcullface**](glcullface.md)
</dt> <dt>

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**gldepthrange**](gldepthrange.md)
</dt> <dt>

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glnebel**](glfog.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**gllight**](gllight-functions.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**gllinestippel**](gllinestipple.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glpolygonmode**](glpolygonmode.md)
</dt> <dt>

[**glpolygonstippel**](glpolygonstipple.md)
</dt> <dt>

[**glscissor**](glscissor.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**gltexgen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





