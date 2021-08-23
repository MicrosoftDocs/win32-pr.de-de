---
title: glFeedbackBuffer-Funktion (Gl.h)
description: Die glFeedbackBuffer-Funktion steuert den Feedbackmodus.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e51a08dac2bbf55509d4964218fc4b844581c797220294464b84c05de5e05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580200"
---
# <a name="glfeedbackbuffer-function"></a>glFeedbackBuffer-Funktion

Die **glFeedbackBuffer-Funktion** steuert den Feedbackmodus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*size* 
</dt> <dd>

Die maximale Anzahl von Werten, die in *den Puffer* geschrieben werden können.

</dd> <dt>

*type* 
</dt> <dd>

Eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgegeben werden. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ COLOR, GL \_ 3D \_ COLOR TEXTURE und GL \_ \_ 4D \_ COLOR \_ TEXTURE.

</dd> <dt>

*Puffer* 
</dt> <dd>

Gibt die Feedbackdaten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* war kein akzeptierter Wert.<br/>                                                                                                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *size* war negativ.<br/>                                                                                                                                                                                        |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | **glFeedbackBuffer** wurde aufgerufen, während der Rendermodus GL \_ FEEDBACK war, oder [**glRenderMode**](glrendermode.md) wurde mit dem Argument GL FEEDBACK aufgerufen, \_ bevor **glFeedbackBuffer** mindestens einmal aufgerufen wurde.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                  |



## <a name="remarks"></a>Hinweise

Die **glFeedbackBuffer-Funktion** steuert Feedback. Feedback ist wie die Auswahl ein OpenGL-Modus. Der Modus wird durch Aufrufen von [**glRenderMode**](glrendermode.md) mit GL \_ FEEDBACK ausgewählt. Wenn sich OpenGL im Feedbackmodus befindet, werden keine Pixel durch Rasterung erzeugt. Stattdessen werden Informationen zu Primitiven, die gerastert worden wären, mithilfe von OpenGL an die Anwendung zurückgespeist.

Die **glFeedbackBuffer-Funktion** verfügt über drei Argumente:

-   *buffer* ist ein Zeiger auf ein Array von Gleitkommawerten, in das Feedbackinformationen platziert werden.
-   *size* gibt die Größe des Arrays an.
-   *type* ist eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgespeist werden.

Sie müssen **glFeedbackBuffer** ausstellen, bevor der Feedbackmodus aktiviert wird (durch Aufrufen von **glRenderMode** mit dem Argument GL \_ FEEDBACK). Das Festlegen von GL \_ FEEDBACK, ohne den Feedbackpuffer einzurichten oder **glFeedbackBuffer** aufzurufen, während sich OpenGL im Feedbackmodus befindet, ist ein Fehler.

Versetzen Sie OpenGL aus dem Feedbackmodus, indem Sie [**glRenderMode**](glrendermode.md) mit einem anderen Parameterwert als GL \_ FEEDBACK aufrufen. Wenn Sie dies tun, während sich OpenGL im Feedbackmodus befindet, gibt **glRenderMode** die Anzahl der Einträge zurück, die im Feedbackarray platziert werden. Der zurückgegebene Wert überschreitet nie die *Größe*. Wenn die Feedbackdaten mehr Platz benötigten, als im *Puffer* verfügbar waren, gibt **glRenderMode** einen negativen Wert zurück.

Im Feedbackmodus generiert jeder Primitive, der gerastert werden würde, einen Block von Werten, der in das Feedbackarray kopiert wird. Wenn dies dazu führen würde, dass die Anzahl der Einträge den Maximalwert überschreitet, schreibt **glFeedbackBuffer** den Block teilweise so, dass er das Array füllt (wenn überhaupt noch Platz vorhanden ist) und legt ein Überlaufflag fest. Jeder Block beginnt mit einem Code, der den primitiven Typ angibt, gefolgt von Werten, die die Scheitelpunkte und die zugeordneten Daten des Primitivs beschreiben. Die **glFeedbackBuffer-Funktion** schreibt auch Einträge für Bitmaps und Pixelrechtecke. Feedback tritt auf, nachdem polygon-culling und [**glPolygonMode-Interpretation**](glpolygonmode.md) von Polygonen stattgefunden haben, sodass Polygone, die aus dem Culling gezogen werden, nicht im Feedbackpuffer zurückgegeben werden. Sie kann auch auftreten, nachdem Polygone mit mehr als drei Kanten in Dreiecke aufgeteilt wurden, wenn die OpenGL-Implementierung Polygone rendert, indem diese Zerlegung ausgeführt wird.

Sie können einen Marker mit [**glPassThrough**](glpassthrough.md)in den Feedbackpuffer einfügen.

Im Folgenden wird die Grammatik für die In den Feedbackpuffer geschriebenen Werteblöcke angegeben. Jeder Primitive wird mit einem eindeutigen identifizierenden Wert gefolgt von einer bestimmten Anzahl von Scheitelpunkten angegeben. Polygoneinträge enthalten einen ganzzahligen Wert, der angibt, wie viele Scheitelpunkte folgen. Ein Scheitelpunkt wird als eine bestimmte Anzahl von Gleitkommawerten zurückgespeist, wie vom *Typ* bestimmt. Farben werden im RGBA-Modus als vier Werte und im Farbindexmodus als ein Wert zurückgespeist.

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < Point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru

Punkt < GL \_ POINT \_ TOKEN-Scheitelpunkt

lineSegment < GL \_ LINE \_ TOKEN vertex vertex \| GL LINE RESET TOKEN \_ \_ \_ vertex vertex

polygon < GL \_ POLYGON \_ TOKEN n polySpec

polySpec < vertex vertex vertex polySpec \| vertex vertex

Bitmap < GL \_ BITMAP \_ TOKEN Vertex

pixelRectangle < GL \_ DRAW \_ PIXEL TOKEN \_ vertex GL COPY PIXEL \| TOKEN \_ \_ \_ vertex

passThru < GL \_ PASS \_ THROUGH \_ TOKEN-Wert

vertex < 2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture

2D < Wert

3D-< Wertwert

3dColor < Wertwertfarbe

3dColorTexture < Wertwert Farbtext

4dColorTexture < Wertwertwert Farbtext

Color < \| RGBA-Index

rgba < Wertwertwert

Index < Werts

Tex < Wertwertwert

Der *Value-Parameter* ist eine Gleitkommazahl, und *n* ist eine ganzzahlige Gleitkommazahl, die die Anzahl der Scheitelpunkte im Polygon angibt. Es folgen symbolische Gleitkommakonstanten: GL \_ POINT \_ TOKEN, GL \_ LINE \_ TOKEN, GL LINE RESET \_ \_ \_ TOKEN, GL POLYGON \_ \_ TOKEN, GL BITMAP \_ \_ TOKEN, GL DRAW PIXEL \_ \_ \_ TOKEN, GL COPY PIXEL \_ TOKEN und GL PASS THROUGH \_ \_ \_ \_ \_ TOKEN. GL \_ LINE RESET TOKEN wird immer dann \_ \_ zurückgegeben, wenn das Linienstipplemuster zurückgesetzt wird. Die als Scheitelpunkt zurückgegebenen Daten hängen vom *Feedbacktyp* ab.

In der folgenden Tabelle wird die Entsprechung zwischen *Typ* und Anzahl der Werte pro Scheitelpunkt angegeben. *k* ist 1 im Farbindexmodus und 4 im RGBA-Modus.



| Typ                   | Koordinaten        | Color | Struktur | Gesamtzahl der Werte |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x,* *y,* *z*      |       |         | 3                      |
| GL \_ 3D \_ COLOR          | *x,* *y,* *z*      | *K*   |         | 3 + *k*                |
| GL \_ 3D \_ COLOR \_ TEXTURE | *x*, *y*, *z*,     | *K*   | 4       | 7 + *k*                |
| GL \_ 4D \_ COLOR \_ TEXTURE | *x*, *y*, *z*, *w* | *K*   | 4       | 8 + *k*                |



 

Feedback-Scheitelpunktkoordinaten befinden sich in Fensterkoordinaten, mit Ausnahme *von w*, das sich in Clipkoordinaten befindet. Feedbackfarben werden hell, wenn die Beleuchtung aktiviert ist. Feedbacktexturkoordinaten werden generiert, wenn die Texturkoordinatengenerierung aktiviert ist. Sie werden immer durch die Texturmatrix transformiert.

Die **glFeedbackBuffer-Funktion** wird bei Verwendung in einer Anzeigeliste nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glFeedbackBuffer** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ RENDER \_ MODE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





