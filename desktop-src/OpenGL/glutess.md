---
title: gluTessCallback-Funktion (Glu.h)
description: Die gluTessCallback-Funktion definiert einen Rückruf für ein Mosaikobjekt.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310ffe6b59e0b3fab307d1103f29c8fe619f0385
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481936"
---
# <a name="glutesscallback-function"></a>gluTessCallback-Funktion

Die **gluTessCallback-Funktion** definiert einen Rückruf für ein Mosaikobjekt.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*welche* 
</dt> <dd>

Der rückruf, der definiert wird. Die folgenden Werte sind gültig: GLU \_ TESS \_ BEGIN, GLU \_ TESS \_ BEGIN \_ DATA, GLU \_ TESS \_ EDGE \_ FLAG, GLU \_ TESS \_ EDGE FLAG \_ \_ DATA, GLU \_ TESS \_ VERTEX, GLU \_ TESS \_ VERTEX \_ DATA, GLU \_ TESS \_ END, GLU \_ TESS \_ END \_ DATA, GLU \_ TESS \_ COMBINE, GLU \_ TESS \_ COMBINE \_ DATA, GLU \_ TESS \_ ERROR und GLU \_ TESS \_ ERROR \_ DATA.

Weitere Informationen zu diesen Rückrufen finden Sie im abschnitt "Hinweise".

</dd> <dt>

*fn* 
</dt> <dd>

Die funktion, die aufgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluTessCallback,** um einen Rückruf anzugeben, der von einem Mosaikobjekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *fn* **NULL** ist, wird der vorhandene Rückruf nicht definiert.

Das Mosaikobjekt verwendet diese Rückrufe, um zu beschreiben, wie ein von Ihnen angegebenes Polygon in Dreiecke unterteilt wird.

Es gibt zwei Versionen jedes Rückrufs: eine mit Polygondaten, die Sie definieren können, und eine ohne . Wenn beide Versionen eines bestimmten Rückrufs angegeben sind, wird der Rückruf mit den von Ihnen angegebenen Polygondaten verwendet. Der *\_ Polygondatenparameter* von [**gluTessBeginPolygon**](glutessbeginpolygon.md) ist eine Kopie des Zeigers, der beim Aufruf von **gluTessBeginPolygon** angegeben wurde.

Es folgen gültige Rückrufe:




| Rückruf | BESCHREIBUNG | 
|----------|-------------|
| GLU_TESS_BEGIN | Der GLU_TESS_BEGIN Rückruf wird wie <a href="glbegin.md"><strong>glBegin</strong></a> aufgerufen, um den Anfang eines Primitiven (Dreieck) anzugeben. Die Funktion nimmt ein einzelnes Argument vom Typ <strong>GLenum</strong>an. Wenn Sie die eigenschaft GLU_TESS_BOUNDARY_ONLY auf GL_FALSE festlegen, wird das Argument entweder auf GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP oder GL_TRIANGLES festgelegt. Wenn Sie die GLU_TESS_BOUNDARY_ONLY-Eigenschaft auf GL_TRUE festlegen, wird das Argument auf GL_LINE_LOOP festgelegt. Der Funktionsprototyp für diesen Rückruf lautet wie folgt: <strong>void</strong><strong>begin</strong> (<strong>GLenum-Typ</strong><em></em>);<br /> | 
| GLU_TESS_BEGIN_DATA | GLU_TESS_BEGIN_DATA entspricht dem GLU_TESS_BEGIN Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>beginData</strong> (<strong>GLenum-Typ</strong><em></em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_EDGE_FLAG | Der GLU_TESS_EDGE_FLAG-Rückruf ähnelt <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. Die Funktion verwendet ein einzelnes boolesches Flag, das angibt, welche Kanten sich an der Polygongrenze befinden. Wenn das Flag GL_TRUE ist, beginnt jeder folgende Scheitelpunkt mit einem Rand, der sich an der Polygongrenze befindet. Das heißt, ein Rand, der einen inneren Bereich von einem äußeren trennt. Wenn das Flag GL_FALSE ist, beginnt jeder folgende Scheitelpunkt mit einem Rand, der im Polygoninneren liegt. Der GLU_TESS_EDGE_FLAG Rückruf (sofern definiert) wird aufgerufen, bevor der erste Scheitelpunktrückruf erfolgt. Da Dreiecksfächer und Dreiecksstreifen keine Edgeflags unterstützen, wird der Startrückruf nicht mit GL_TRIANGLE_FAN oder GL_TRIANGLE_STRIP aufgerufen, wenn ein Edgeflagrückruf bereitgestellt wird. Stattdessen werden die Lüfter und Strips in unabhängige Dreiecke konvertiert. Der Funktionsprototyp für diesen Rückruf lautet:<br /><strong>void</strong><strong>edgeFlag</strong> (<strong>GLboolean</strong><em>flag</em>);<br /> | 
| GLU_TESS_EDGE_FLAG_DATA | Der GLU_TESS_EDGE_FLAG_DATA-Rückruf entspricht dem GLU_TESS_EDGE_FLAG Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>edgeFlagData</strong> (<strong>GLboolean</strong><em>flag</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_VERTEX | Der GLU_TESS_VERTEX Rückruf wird zwischen den Start- und Endrückrufen aufgerufen. Sie ähnelt glVertex und definiert die Scheitelpunkte der Dreiecke, die durch den Mosaikprozess erstellt werden. Die Funktion verwendet einen Zeiger als einziges Argument. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, den Sie beim Definieren des Scheitelpunkts angegeben haben (siehe <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>vertex</strong> (<strong>void</strong>  *  <em>vertex_data</em>);<br /> | 
| GLU_TESS_VERTEX_DATA | Die GLU_TESS_VERTEX_DATA entspricht dem GLU_TESS_VERTEX Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_END | Der GLU_TESS_END-Rückruf dient dem gleichen Zweck wie <a href="glend.md"><strong>glEnd.</strong></a> Er gibt das Ende eines Primitiven an und nimmt keine Argumente an. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>end</strong> (<strong>void</strong>);<br /> | 
| GLU_TESS_END_DATA | Der GLU_TESS_END_DATA-Rückruf entspricht dem GLU_TESS_END Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>endData</strong> (<strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_COMBINE | Rufen Sie den GLU_TESS_COMBINE Rückruf auf, um einen neuen Scheitelpunkt zu erstellen, wenn das Mosaik eine Schnittmenge erkennt, oder um Features zusammenzuführen. Die Funktion verwendet vier Argumente: ein Array von drei Elementen vom Typ Gldouble.<br /> Ein Array von vier Zeigern.<br /> Ein Array von vier Elementen vom Typ GLfloat.<br /> Ein Zeiger auf einen Zeiger.<br /> Der Funktionsprototyp für diesen Rückruf lautet: <br /><strong>void</strong><strong>combine</strong>(<strong>GLdouble</strong><em>coords</em>[3], <strong>void</strong>  *  <em>vertex_data</em>[4], <strong>GLfloat</strong><em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>);<br /> Der Scheitelpunkt wird als lineare Kombination von bis zu vier vorhandenen Scheitelpunkten definiert, die in vertex_data gespeichert sind. Die Koeffizienten der linearen Kombination werden nach Gewichtung angegeben. diese Gewichtungen summieren sich immer auf 1,0. Alle Scheitelpunktzeiger sind auch dann gültig, wenn einige der Gewichtungen 0 (null) sind. Der Coords-Parameter gibt die Position des neuen Scheitelpunkts an.<br /> Ordnen Sie einen weiteren Scheitelpunkt zu, interpolieren Sie Parameter mit vertex_data und Gewichtung, und geben Sie den neuen Scheitelpunktzeiger in outData zurück. Dieses Handle wird bei Renderingrückrufen bereitgestellt. Freigeben des Arbeitsspeichers nach dem Aufruf von <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br /> Wenn das Polygon beispielsweise in einer beliebigen Ebene im dreidimensionalen Raum liegt und Sie jedem Scheitelpunkt eine Farbe zuordnen, könnte der GLU_TESS_COMBINE Rückruf wie folgt aussehen:<br /><pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4],                 GLfloat w[4], VERTEX **dataOut ) {     VERTEX *newVertex = new_vertex();     newVertex-&gt;x = coords[0];     newVertex-&gt;y = coords[1];     newVertex-&gt;z = coords[2];     newVertex-&gt;r = w[0]*d[0]-&gt;r + w[1]*d[1]-&gt;r + w[2]*d[2]-&gt;r +                    w[3]*d[3]-&gt;r;     newVertex-&gt;g = w[0]*d[0]-&gt;g + w[1]*d[1]-&gt;g + w[2]*d[2]-&gt;g +                    w[3]*d[3]-&gt;g;     newVertex-&gt;b = w[0]*d[0]-&gt;b + w[1]*d[1]-&gt;b + w[2]*d[2]-&gt;b +                    w[3]*d[3]-&gt;b;     newVertex-&gt;a = w[0]*d[0]-&gt;a + w[1]*d[1]-&gt;a + w[2]*d[2]-&gt;a +                    w[3]*d[3]-&gt;a;     *dataOut = newVertex; }</code></pre>Wenn das Mosaik eine Schnittmenge erkennt, muss der GLU_TESS_COMBINE- oder GLU_TESS_COMBINE_DATA-Rückruf (siehe unten) definiert werden und einen<strong>Ungleich-NULL-Zeiger</strong> in dataOut schreiben. Andernfalls tritt der GLU_TESS_NEED_COMBINE_CALLBACK Fehler auf, und es wird keine Ausgabe generiert. (Dies ist der einzige Fehler, der während des Mosaiks und Renderings auftreten kann.)<br /> | 
| GLU_TESS_COMBINE_DATA | Der GLU_TESS_COMBINE_DATA-Rückruf entspricht dem GLU_TESS_COMBINE Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>combineData</strong> (<strong>GLdouble</strong><em>coords</em>[3], <strong>void</strong>  * <em>vertex_data</em>[4], <strong>GLfloat</strong><em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_ERROR | Der GLU_TESS_ERROR Rückruf wird aufgerufen, wenn ein Fehler auftritt. Das ein Argument ist vom Typ <strong>GLenum</strong>; gibt den spezifischen Fehler an, der aufgetreten ist, und wird auf eine der folgenden Festgelegt: GLU_TESS_MISSING_BEGIN_POLYGON<br /> GLU_TESS_MISSING_END_POLYGON<br /> GLU_TESS_MISSING_BEGIN_CONTOUR<br /> GLU_TESS_MISSING_END_CONTOUR<br /> GLU_TESS_COORD_TOO_LARGE<br /> GLU_TESS_NEED_COMBINE_CALLBACK<br /> Rufen Sie gluErrorString auf, um Zeichenfolgen abzurufen, die diese Fehler beschreiben. Der Funktionsprototyp für diesen Rückruf lautet wie folgt:<br /><strong>void</strong><strong>error</strong> (<strong>GLenum</strong><em>errno</em>);<br /> Die GLU-Bibliothek stellt die ersten vier Fehler wieder her, indem der fehlende Aufruf oder die fehlenden Aufrufe eingefügt werden. GLU_TESS_COORD_TOO_LARGE gibt an, dass eine Scheitelpunktkoordinate die vordefinierte Konstante GLU_TESS_MAX_COORD im absoluten Wert überschritten hat und dass der Wert geklammert wurde. (Koordinatenwerte müssen klein genug sein, damit zwei ohne Überlauf multipliziert werden können.) GLU_TESS_NEED_COMBINE_CALLBACK gibt an, dass das Mosaik eine Schnittmenge zwischen zwei Kanten in den Eingabedaten erkannt hat und der GLU_TESS_COMBINE oder GLU_TESS_COMBINE_DATA Rückruf nicht bereitgestellt wurde. Es wird keine Ausgabe generiert.<br /> | 
| GLU_TESS_ERROR_DATA | Der GLU_TESS_ERROR_DATA Rückruf entspricht dem GLU_TESS_ERROR Rückruf, außer dass ein zusätzliches Zeigerargument verwendet wird. Dieser Zeiger ist identisch mit dem nicht transparenten Zeiger, der beim Aufrufen von <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong><strong>errorData</strong> (<strong>GLenum</strong><em>errno</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 




 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





