---
title: glutesscallback-Funktion (glu. h)
description: Die Funktion "glutesscallback" definiert einen Rückruf für ein Mosaik Objekt.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- glutesscallback-Funktion OpenGL
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
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957076"
---
# <a name="glutesscallback-function"></a>glutesscallback-Funktion

Die Funktion " **glutesscallback** " definiert einen Rückruf für ein Mosaik Objekt.

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

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*,* 
</dt> <dd>

Der Rückruf, der definiert wird. Die folgenden Werte sind gültig: glu \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, Glu \_ Tess \_ Edge \_ Flag, Glu \_ Tess \_ Edge \_ \_ flagdaten, Glu \_ Tess \_ Vertex, Glu \_ Tess \_ Vertex \_ Data, Glu \_ Tess \_ End, Glu \_ Tess \_ End \_ Data, Glu \_ Tess \_ Combine, Glu \_ Tess \_ Combine \_ Data, Glu \_ Tess \_ Error und glu \_ Tess- \_ Fehler \_ Daten.

Weitere Informationen zu diesen Rückrufen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*fn* 
</dt> <dd>

Die aufzurufende Funktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glutesscallback** ", um einen Rückruf anzugeben, der von einem Mosaik Objekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *FN* **null** ist, wird der vorhandene Rückruf nicht definiert.

Das Mosaik Objekt verwendet diese Rückrufe, um zu beschreiben, wie ein Polygon, das Sie angeben, in Dreiecke unterteilt wird.

Es gibt zwei Versionen der einzelnen Rückruf, eine mit Polygon Daten, die Sie definieren können, und eine, ohne. Wenn beide Versionen eines bestimmten Rückrufs angegeben werden, wird der Rückruf mit den von Ihnen angegebenen Polygon Daten verwendet. Der *Polygon- \_ Daten* Parameter von " [**glutess beginpolygon**](glutessbeginpolygon.md) " ist eine Kopie des Zeigers, der beim Aufruf von " **glutess beginpolygon** " angegeben wurde.

Im folgenden finden Sie gültige Rückrufe:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückruf</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>Der GLU_TESS_BEGIN Rückruf wird wie " <a href="glbegin.md"><strong>glBegin</strong></a> " aufgerufen, um den Anfang eines primitiven (Dreiecks) anzugeben. Die Funktion nimmt ein einzelnes Argument des Typs " <strong>GLenum</strong>" an. Wenn Sie die GLU_TESS_BOUNDARY_ONLY-Eigenschaft auf GL_FALSE festlegen, wird das-Argument entweder auf GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP oder GL_TRIANGLES festgelegt. Wenn Sie die GLU_TESS_BOUNDARY_ONLY-Eigenschaft auf GL_TRUE festlegen, wird das-Argument auf GL_LINE_LOOP festgelegt. Der Funktionsprototyp für diesen Rückruf lautet wie folgt: <strong>void</strong> <strong>Begin</strong> (<strong>GLenum</strong> <em>Type</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA ist mit dem GLU_TESS_BEGIN Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>begindata</strong> (<strong>GLenum</strong> <em>Type</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>Der GLU_TESS_EDGE_FLAG Rückruf ähnelt dem <a href="gledgeflag-functions.md"><strong>gledgeflag</strong></a>. Die Funktion nimmt ein einzelnes boolesches Flag an, das angibt, welche Ränder auf der Polygon Grenze liegen. Wenn das Flag GL_TRUE ist, beginnt jeder nachfolgende Scheitelpunkt mit einem Rand, der sich auf der Polygon Grenze befindet. Das heißt, ein Rand, der einen inneren Bereich von einem äußeren Bereich trennt. Wenn das Flag GL_FALSE ist, beginnt jeder nachfolgende Scheitelpunkt mit einem Rand im Polygon Inneren. Der GLU_TESS_EDGE_FLAG Rückruf (falls definiert) wird aufgerufen, bevor der erste Vertex-Rückruf erfolgt. Da Dreiecks Lüfter und Dreieck Striche keine Edge-Flags unterstützen, wird der BEGIN-Rückruf nicht mit GL_TRIANGLE_FAN oder GL_TRIANGLE_STRIP aufgerufen, wenn ein Edge-Flag-Rückruf bereitgestellt wird. Stattdessen werden die Lüfter und die Striche in unabhängige Dreiecke konvertiert. Der Funktionsprototyp für diesen Rückruf ist:<br/> <strong>void</strong> <strong>edgeflag</strong> (<strong>glboolean</strong> - <em>Flag</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>Der GLU_TESS_EDGE_FLAG_DATA Rückruf ist mit dem GLU_TESS_EDGE_FLAG Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>edgeflagdata</strong> (<strong>glboolean</strong> - <em>Flag</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>Der GLU_TESS_VERTEX Rückruf wird zwischen den Anfang-und endrückrufen aufgerufen. Sie ähnelt glVertex und definiert die vertexen der Dreiecke, die vom Mosaik Prozess erstellt werden. Die Funktion nimmt einen Zeiger als einziges Argument an. Dieser Zeiger ist mit dem nicht transparenten Zeiger identisch, den Sie beim Definieren des Scheitel Punkts angegeben haben (siehe " <a href="glutessvertex.md"><strong>glutess Scheitel</strong></a>Punkt"). Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>Scheitel</strong> Punkt (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>Der GLU_TESS_VERTEX_DATA ist mit dem GLU_TESS_VERTEX Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong>  <strong>vertexdata</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>Der GLU_TESS_END Rückruf erfüllt den gleichen Zweck wie <a href="glend.md"><strong>glEnd</strong></a>. Er gibt das Ende eines primitiven an und übernimmt keine Argumente. Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>End</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>Der GLU_TESS_END_DATA Rückruf ist mit dem GLU_TESS_END Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Rufen Sie den GLU_TESS_COMBINE Rückruf auf, um einen neuen Scheitelpunkt zu erstellen, wenn das Mosaik eine Schnittmenge erkennt, oder um die Funktionen zusammenzuführen. Die Funktion nimmt vier Argumente an: ein Array mit drei Elementen, jeweils vom Typ gldouble.<br/> Ein Array von vier Zeigern.<br/> Ein Array von vier Elementen, jeweils vom Typ "glfloat".<br/> Ein Zeiger auf einen Zeiger.<br/> Der Funktionsprototyp für diesen Rückruf ist: <br/> <strong>void</strong> <strong>Combine</strong>(<strong>gldouble</strong> <em>CoOrds</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong>glfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>OutData</em>);<br/> Der Scheitelpunkt ist eine lineare Kombination aus bis zu vier vorhandenen vertexen, die in vertex_data gespeichert werden. Die Koeffizienten der linearen Kombination werden durch Gewichtung angegeben. Diese Gewichtungen summieren immer auf 1,0. Alle Scheitelpunkt Zeiger sind gültig, auch wenn einige der Gewichtungen NULL sind. Der CoOrds-Parameter gibt den Speicherort des neuen Scheitel Punkts an.<br/> Weisen Sie einen anderen Scheitelpunkt zu, interpolieren Sie Parameter mit vertex_data und Gewichtung, und geben Sie den neuen Scheitelpunkt Zeiger in OutData zurück. Dieses Handle wird während der Rendering-Rückrufe bereitgestellt. Freigeben von Arbeitsspeicher nach dem Aufrufen von " <a href="glutessendpolygon.md"><strong>glutessendpolygon</strong></a>".<br/> Wenn das Polygon z. b. in einer beliebigen Ebene im dreidimensionalen Raum liegt und Sie jedem Scheitelpunkt eine Farbe zuordnen, könnte der GLU_TESS_COMBINE Rückruf wie folgt aussehen:<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
Wenn das Mosaik eine Schnittmenge erkennt, muss die GLU_TESS_COMBINE oder GLU_TESS_COMBINE_DATA Rückrufs (siehe unten) definiert sein, und es muss ein nicht-<strong>null</strong> -Zeiger in dataout geschrieben werden. Andernfalls tritt der GLU_TESS_NEED_COMBINE_CALLBACK Fehler auf, und es wird keine Ausgabe generiert. (Dies ist der einzige Fehler, der während des Mosaik-und Renderings auftreten kann.)<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>Der GLU_TESS_COMBINE_DATA Rückruf ist mit dem GLU_TESS_COMBINE Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf ist " <strong>void</strong> <strong>combinedata</strong> (<strong>gldouble</strong> <em>CoOrds</em>[3]", " <strong>void</strong> *<em>vertex_data</em>[4]", " <strong>glfloat</strong> <em>Weight</em>[4]", " <strong>void</strong>  ** <em>OutData</em>", " <strong>void</strong> * <em>polygon_data</em>");<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>Der GLU_TESS_ERROR Rückruf wird aufgerufen, wenn ein Fehler auftritt. Das einzige Argument ist vom Typ " <strong>GLenum</strong>". Gibt den spezifischen Fehler an, der aufgetreten ist, und wird auf einen der folgenden festgelegt: GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Rufen Sie zum Abrufen von Zeichen folgen, die diese Fehler beschreiben, die Zeichen folgen auf. Der Funktionsprototyp für diesen Rückruf lautet wie folgt:<br/> <strong>void</strong> - <strong>Fehler</strong> (<strong>GLenum</strong> <em>errno</em>);<br/> Die glu-Bibliothek stellt die ersten vier Fehler wieder her, indem Sie den fehlenden Aufruf oder die fehlenden Aufrufe einfügt. GLU_TESS_COORD_TOO_LARGE gibt an, dass die Vertex-Koordinate die vordefinierte Konstante GLU_TESS_MAX_COORD in absoluten Wert überschritten hat und dass der Wert gebunden wurde. (Koordinaten Werte müssen klein genug sein, damit zwei ohne Überlauf multipliziert werden können.) GLU_TESS_NEED_COMBINE_CALLBACK gibt an, dass das Mosaik eine Überschneidung zwischen zwei Kanten in den Eingabedaten erkannt hat und der GLU_TESS_COMBINE oder GLU_TESS_COMBINE_DATA Rückruf nicht bereitgestellt wurde. Es wird keine Ausgabe generiert.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>Der GLU_TESS_ERROR_DATA Rückruf ist mit dem GLU_TESS_ERROR Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt. Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird. Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**gledgeflag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gludeletetess**](gludeletetess.md)
</dt> <dt>

[**gluerrorstring**](gluerrorstring.md)
</dt> <dt>

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glutess beginpolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**glutessendpolygon**](glutessendpolygon.md)
</dt> <dt>

[**glutess Vertex**](glutessvertex.md)
</dt> </dl>

 

 





