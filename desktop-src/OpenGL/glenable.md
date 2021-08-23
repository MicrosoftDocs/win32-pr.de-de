---
title: glEnable-Funktion (Gl.h)
description: Die Funktionen glEnable und glDisable aktivieren oder deaktivieren OpenGL-Funktionen. | glEnable-Funktion (Gl.h)
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
ms.openlocfilehash: d4ef13323f72efd516a0c5321cb410885904ac5245b5198b21ea9e4a4b29f3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625630"
---
# <a name="glenable-function"></a>glEnable-Funktion

Die **Funktionen glEnable** und [**glDisable**](gldisable.md) aktivieren oder deaktivieren OpenGL-Funktionen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cap* 
</dt> <dd>

Eine symbolische Konstante, die eine OpenGL-Funktion angibt.

Informationen zur Werteobergrenze *finden* Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *cap* war nicht einer der Im vorherigen Abschnitt "Hinweise" aufgeführten Werte.<br/>                                                   |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **Funktionen glEnable** **und glDisable** aktivieren und deaktivieren verschiedene OpenGL-Grafikfunktionen. Verwenden [**Sie glIsEnabled oder**](glisenabled.md) [**glGet,**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) um die aktuelle Einstellung einer Funktion zu bestimmen.

Sowohl **glEnable als** **auch glDisable** verwenden ein einzelnes Argument, *cap,* das einen der folgenden Werte annehmen kann:



| Wert                       | Bedeutung                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ \_ ALPHA-TEST             | Wenn diese Option aktiviert ist, sollten Sie Alphatests durchführen. Siehe [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ AUTO \_ NORMAL            | Wenn aktiviert, berechnen Sie normale Oberflächenvektoren analystisch, wenn GL \_ MAP2 \_ VERTEX 3 oder \_ GL \_ MAP2 \_ VERTEX \_ 4 Scheitelpunkte generiert haben. Siehe [**glMap2**](glmap2.md).                                                                                        |
| GL \_ BLEND                   | Wenn aktiviert, mischen Sie die eingehenden RGBA-Farbwerte mit den Werten in den Farbpuffern. Siehe [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| GL \_ CLIP \_ PLANE *i*          | Wenn diese Option aktiviert ist, wird die Geometrie mit der benutzerdefinierten Clippingebene *i abgeschnitten.* Weitere Informationen [**finden Sie unter glClipPlane**](glclipplane.md).                                                                                                                                                  |
| GL \_ COLOR \_ LOGIC \_ OP        | Wenn diese Option aktiviert ist, wenden Sie den aktuellen logischen Vorgang auf die eingehenden RGBA-Farb- und Farbpufferwerte an. Siehe [**glLogicOp**](gllogicop.md).                                                                                                                     |
| GL \_ COLOR \_ MATERIAL         | Wenn aktiviert, lassen Sie einen oder mehrere Materialparameter die aktuelle Farbe nachverfolgen. Siehe [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| GL \_ CULL \_ FACE              | Wenn aktiviert, cull polygons based on their winding in window coordinates. Siehe [**glCullFace**](glcullface.md).                                                                                                                                               |
| GL \_ DEPTH \_ TEST             | Wenn diese Option aktiviert ist, sollten Sie tiefenvergleiche und den Tiefenpuffer aktualisieren. Siehe [**glDepthFunc**](gldepthfunc.md) und [**glDepthRange**](gldepthrange.md).                                                                                                              |
| GL \_ DITHER                  | Wenn diese Option aktiviert ist, geben Sie die Farbkomponenten oder -indizes ein, bevor sie in den Farbpuffer geschrieben werden.                                                                                                                                                                 |
| GL \_ FOG                     | Wenn diese Option aktiviert ist, blenden Sie eine Farbe in die Farbe nach der Textur ein. Siehe [**glFog**](glfog.md).                                                                                                                                                                    |
| GL \_ INDEX \_ LOGIC \_ OP        | Wenn diese Option aktiviert ist, wenden Sie den aktuellen logischen Vorgang auf den eingehenden Index und die Farbpufferindizes an. Siehe [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ LIGHT *i*                | Wenn diese Option aktiviert ist, schließen Sie licht *i* in die Auswertung der Beleuchtungsgleichung ein. Weitere Informationen [**finden Sie unter glLightModel**](gllightmodel-functions.md) [**und glLight.**](gllight-functions.md)                                                                                      |
| GL \_ LIGHTING                | Wenn diese Option aktiviert ist, verwenden Sie die aktuellen Beleuchtungsparameter, um die Scheitelpunktfarbe oder den Scheitelpunktindex zu berechnen. Wenn deaktiviert, ordnen Sie jedem Scheitelpunkt die aktuelle Farbe oder den aktuellen Index zu. Siehe [**glMaterial**](glmaterial-functions.md), **glLightModel** und **glLight**.                |
| GL \_ LINE \_ SMOOTH            | Wenn diese Option aktiviert ist, zeichnen Sie Linien mit korrekter Filterung. Wenn deaktiviert, zeichnen Sie Aliaslinien. Siehe [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| GL \_ LINE \_ STIPPLE           | Wenn diese Option aktiviert ist, verwenden Sie beim Zeichnen von Linien das aktuelle Zeilenausschnittmuster. Siehe [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| GL \_ LOGIC \_ OP               | Wenn diese Option aktiviert ist, wenden Sie den derzeit ausgewählten logischen Vorgang auf die eingehenden Indizes und farbpufferbasierten Indizes an. Siehe [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1 \_ COLOR \_ 4          | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) RGBA-Werte. Siehe auch [**glMap1**](glmap1.md).                                           |
| GL \_ MAP1 \_ INDEX             | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord1,** **glEvalMesh1** und **glEvalPoint1** Farbindizes. Siehe auch **glMap1**.                                                                                                                                   |
| GL \_ MAP1 \_ NORMAL            | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) Normals. Siehe auch [**glMap1**](glmap1.md).                                               |
| GL \_ MAP1 \_ \_ TEXTURKOORD \_ 1 | Wenn aktiviert, generieren **Aufrufe von glEvalCoord1,** **glEvalMesh1** und **glEvalPoint1** *die* Texturkoordinaten. Siehe auch **glMap1**.                                                                                                                         |
| GL \_ MAP1 \_ \_ TEXTURKOORD \_ 2 | Wenn aktiviert, generieren Aufrufe von [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) *s-* und t-Texturkoordinaten.  Siehe auch [**glMap1**](glmap1.md).                       |
| GL \_ MAP1 \_ \_ TEXTURKOORD \_ 3 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord1,** **glEvalMesh1** und **glEvalPoint1** die Texturkoordinaten *,* *t* und *r.* Siehe auch **glMap1**.                                                                                                           |
| GL \_ MAP1 \_ \_ TEXTURKOORD \_ 4 | Wenn diese Option aktiviert ist, generieren Aufrufe von [glEvalCoord1,](glevalcoord-functions.md) [glEvalMesh1](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) die Texturkoordinaten *,* *t,* *r* und *q.* Siehe auch [**glMap1**](glmap1.md).                    |
| GL \_ MAP1 \_ VERTEX \_ 3         | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord1,** **glEvalMesh1** und **glEvalPoint1** *x-,* *y-* und z-Vertexkoordinaten.  Siehe auch **glMap1**.                                                                                                            |
| GL \_ MAP1 \_ VERTEX \_ 4         | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)und [**glEvalPoint1**](glevalpoint.md) homogene *x-,* *y-,* *z-* und w-Scheitelpunktkoordinaten.  Siehe auch [**glMap1.**](glmap1.md) |
| GL \_ MAP2 \_ COLOR \_ 4          | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) RGBA-Werte. Siehe auch [**glMap2.**](glmap2.md)                                           |
| GL \_ MAP2 \_ INDEX             | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2,** **glEvalMesh2** und **glEvalPoint2** Farbindizes. Siehe auch **glMap2.**                                                                                                                                   |
| GL \_ MAP2 \_ NORMAL            | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) Normaldaten. Siehe auch [**glMap2.**](glmap2.md)                                               |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2,** **glEvalMesh2** und **glEvalPoint2** Texturkoordinaten.  Siehe auch **glMap2.**                                                                                                                         |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2 | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) *die* Texturkoordinaten s und *t.* Siehe auch [**glMap2.**](glmap2.md)                       |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3 | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2,** **glEvalMesh2** und **glEvalPoint2** *die* Texturkoordinaten s , *t* und *r.* Siehe auch **glMap2.**                                                                                                           |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4 | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) die Texturkoordinaten *s*, *t*, *r* und *q.* Siehe auch [**glMap2.**](glmap2.md)            |
| GL \_ MAP2 \_ VERTEX \_ 3         | Wenn diese Option aktiviert ist, generieren Aufrufe von **glEvalCoord2,** **glEvalMesh2** und **glEvalPoint2** *x-,* *y-* und z-Scheitelpunktkoordinaten.  Siehe auch **glMap2.**                                                                                                            |
| GL \_ MAP2 \_ VERTEX \_ 4         | Wenn diese Option aktiviert ist, generieren Aufrufe von [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)und [**glEvalPoint2**](glevalpoint.md) *homogene* x-, *y-,* *z-* und w-Scheitelpunktkoordinaten.  Siehe auch [**glMap2.**](glmap2.md) |
| GL \_ NORMALIZE               | Wenn diese Option aktiviert ist, werden normal mit **glNormal** angegebene Vektoren nach der Transformation auf die Einheitslänge skaliert. Siehe [**glNormal**](glnormal-functions.md).                                                                                                          |
| GL \_ POINT \_ SMOOTH           | Wenn diese Option aktiviert ist, zeichnen Sie Punkte mit ordnungsgemäßer Filterung. Wenn diese Option deaktiviert ist, zeichnen Sie Punkte mit Alias. Siehe [**glPointSize**](glpointsize.md).                                                                                                                                    |
| GL \_ POLYGON \_ OFFSET \_ FILL   | Wenn diese Option aktiviert ist und das Polygon im GL FILL-Modus gerendert \_ wird, wird den Tiefenwerten der Fragmente eines Polygons ein Offset hinzugefügt, bevor der Tiefenvergleich durchgeführt wird. Siehe [**glPolygonOffset.**](glpolygonoffset.md)                                      |
| GL \_ POLYGON \_ OFFSET \_ LINE   | Wenn diese Option aktiviert ist und das Polygon im GL LINE-Modus gerendert \_ wird, wird den Tiefenwerten der Fragmente eines Polygons ein Offset hinzugefügt, bevor der Tiefenvergleich durchgeführt wird. Siehe **glPolygonOffset.**                                                                 |
| GL \_ POLYGON \_ OFFSET \_ POINT  | Wenn diese Option aktiviert ist, wird den Tiefenwerten der Fragmente eines Polygons vor dem Tiefenvergleich ein Offset hinzugefügt, wenn das Polygon im GL POINT-Modus gerendert \_ wird. Siehe [**glPolygonOffset.**](glpolygonoffset.md)                                             |
| GL \_ POLYGON \_ SMOOTH         | Wenn diese Option aktiviert ist, zeichnen Sie Polygone mit ordnungsgemäßer Filterung. Wenn diese Option deaktiviert ist, zeichnen Sie Polygone mit Alias. Siehe [**glPolygonMode.**](glpolygonmode.md)                                                                                                                            |
| GL \_ POLYGON \_ STIPPLE        | Wenn diese Option aktiviert ist, verwenden Sie beim Rendern von Polygonen das aktuelle Polygonstipplemuster. Siehe [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| GL \_ \_ SCISSOR-TEST           | Wenn diese Option aktiviert ist, verwerfen Sie Fragmente, die sich außerhalb des Scissor-Rechtecks befinden. Siehe [**glScissor**](glscissor.md).                                                                                                                                                   |
| GL \_ \_ STENCIL-TEST           | Wenn diese Option aktiviert ist, können Sie Schablonentests durchführen und den Schablonenpuffer aktualisieren. Siehe [**glStencilFunc**](glstencilfunc.md) und [**glStencilOp**](glstencilop.md).                                                                                                            |
| GL \_ TEXTURE \_ 1D             | Wenn diese Option aktiviert ist, wird die eindimensionale Texturierung ausgeführt (es sei denn, die zweidimensionale Texturierung ist ebenfalls aktiviert). Siehe [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| GL \_ TEXTURE \_ 2D             | Wenn diese Option aktiviert ist, wird die zweidimensionale Texturierung ausgeführt. Siehe [**glTexImage2D.**](glteximage2d.md)                                                                                                                                                               |
| GL \_ TEXTURE \_ GEN \_ Q         | Wenn diese Option aktiviert ist, wird die Texturkoordinate *q* mithilfe der Texturgenerierungsfunktion berechnet, die mit [**glTexGen**](gltexgen-functions.md)definiert ist. Andernfalls  wird die aktuelle q-Texturkoordinate verwendet.                                                        |
| GL \_ TEXTURE \_ GEN \_ R         | Wenn diese  Option aktiviert ist, wird die r-Texturkoordinate mithilfe der Texturgenerierungsfunktion berechnet, die mit [**glTexGen**](gltexgen-functions.md)definiert ist. Wenn diese Option  deaktiviert ist, wird die aktuelle r-Texturkoordinate verwendet.                                                      |
| GL \_ TEXTURE \_ GEN \_ S         | Wenn diese Option aktiviert ist, wird die Texturkoordinate mithilfe der *Texturgenerierungsfunktion* berechnet, die mit **glTexGen** definiert ist. Wenn diese Option deaktiviert ist, wird die *Texturkoordinate* der aktuellen verwendet.                                                                                |
| GL \_ TEXTURE \_ GEN \_ T         | Wenn diese Option aktiviert ist, wird die Texturkoordinate *t* mithilfe der texturgenerierungsfunktion berechnet, die mit [**glTexGen**](gltexgen-functions.md)definiert ist. Wenn diese Option deaktiviert ist, wird die aktuelle *t* Texturkoordinate verwendet.                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





