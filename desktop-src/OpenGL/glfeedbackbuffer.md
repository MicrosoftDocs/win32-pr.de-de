---
title: glfeedbackbuffer-Funktion (GL. h)
description: Die Funktion "glfeedbackbuffer" steuert den Feedback Modus.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glfeedbackbuffer-Funktion OpenGL
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
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343452"
---
# <a name="glfeedbackbuffer-function"></a>glfeedbackbuffer-Funktion

Die Funktion " **glfeedbackbuffer** " steuert den Feedback Modus.

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

Die maximale Anzahl von Werten, die in den *Puffer* geschrieben werden können.

</dd> <dt>

*type* 
</dt> <dd>

Eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgegeben werden. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ Color, GL \_ 3D \_ Color \_ Texture und GL \_ 4D \_ Color \_ Texture.

</dd> <dt>

*ert* 
</dt> <dd>

Gibt die Feedback Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Typ* war kein akzeptierter Wert.<br/>                                                                                                                                                                           |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | die *Größe* war negativ.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | **glfeedbackbuffer** wurde aufgerufen, während der \_ Rendermodus "GL Feedback" war, oder " [**glrendermode**](glrendermode.md) " wurde mit dem Argument "GL Feedback" aufgerufen, \_ bevor " **glfeedbackbuffer** " mindestens einmal aufgerufen wurde.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                  |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glfeedbackbuffer** " steuert das Feedback. Feedback, wie z. b. Auswahl, ist ein OpenGL-Modus. Der Modus wird durch Aufrufen von [**glrendermode**](glrendermode.md) mit GL- \_ Feedback ausgewählt. Wenn OpenGL im Feedback Modus ist, werden von der rasterisierung keine Pixel erzeugt. Stattdessen werden Informationen über primitive, die gerengt worden wären, über OpenGL an die Anwendung zurückgegeben.

Die **glfeedbackbuffer** -Funktion hat drei Argumente:

-   *buffer* ist ein Zeiger auf ein Array von Gleit Komma Werten, in die Feedback Informationen eingefügt werden.
-   *size* gibt die Größe des Arrays an.
-   *Type* ist eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgeleitet werden.

Sie müssen **glfeedbackbuffer** ausgeben, bevor der Feedback Modus aktiviert ist (durch Aufrufen von **glrendermode** mit dem Argument GL- \_ Feedback). Wenn Sie \_ das GL-Feedback ohne Einrichtung des Feedback Puffers festlegen oder " **glfeedbackbuffer** " aufrufen, während sich OpenGL im Feedback Modus befindet, ist ein Fehler aufgetreten.

Akzeptieren Sie OpenGL aus dem Feedback Modus, indem Sie [**glrendermode**](glrendermode.md) mit einem anderen Parameterwert als GL- \_ Feedback aufrufen. Wenn sich OpenGL im Feedback Modus befindet, gibt " **glrendermode** " die Anzahl der Einträge zurück, die im Feedback-Array abgelegt werden. Der zurückgegebene Wert überschreitet nie die *Größe*. Wenn die Feedback Daten mehr Platz benötigen, als im *Puffer* verfügbar waren, gibt **glrendermode** einen negativen Wert zurück.

Im Feedback Modus generiert jedes primitive, das gerastertes wäre, einen Block von Werten, die in das Feedback Array kopiert werden. Wenn dies dazu führen würde, dass die Anzahl der Einträge den maximalen Wert überschreitet, schreibt **glfeedbackbuffer** den Block teilweise so, dass er das Array ausfüllen soll (wenn überhaupt ein Platz übrig ist), und legt ein Überlauf Kennzeichen fest. Jeder Block beginnt mit einem Code, der den primitiven Typ anzeigt, gefolgt von Werten, die die Scheitel Punkte und zugeordneten Daten des primitiven beschreiben. Die **glfeedbackbuffer** -Funktion schreibt auch Einträge für Bitmaps und Pixel Rechtecke. Das Feedback tritt auf, nachdem die Polygon-und [**glpolygonmode**](glpolygonmode.md) -Interpretation von Polygonen stattfindet, sodass Polygone, die als herausgefiltert werden dienen, nicht im Feedback Puffer zurückgegeben werden. Sie kann auch auftreten, nachdem Polygone mit mehr als drei Rändern in Dreiecke aufgeteilt wurden, wenn die OpenGL-Implementierung Polygone durch Ausführen dieser Zerlegung rendert.

Sie können einen Marker mit [**glpassthrough**](glpassthrough.md)in den Feedback Puffer einfügen.

Im folgenden finden Sie die Grammatik für die Blöcke der Werte, die in den Feedback Puffer geschrieben wurden. Jede primitive wird durch einen eindeutigen identifizierenden Wert gefolgt von einer bestimmten Anzahl von Vertices angegeben. Polygon Einträge enthalten einen ganzzahligen Wert, der angibt, wie viele Scheitel Punkte folgen. Ein Scheitelpunkt wird als eine Reihe von Gleit Komma Werten zurückgeführt, die vom *Typ* bestimmt werden. Farben werden als vier Werte im RGBA-Modus und ein Wert im Farb Index Modus zurückgeführt.

feedbacklist < feedbacklist feedbacklist- \| feedbackitem

feedbackitem < Punkt- \| LineSegment \| Polygon \| Bitmap \| Pixel Rechteck \| passthru

Punkt < GL \_ - \_ punkttokenscheitel Punkt

LineSegment < GL- \_ Zeilen Token Vertex-Vertex- \_ \| \_ Zeilen Zurücksetzungs \_ Token- \_ vertexscheitel Punkt

Polygon-< GL- \_ Polygon- \_ Token n polyspec

polyspec < polyspec Scheitelpunkt Scheitelpunkt Scheitelpunkt Scheitelpunkt \|

Bitmap < GL- \_ \_ bitmaptokenscheitel Punkt

Pixel Rechteck < GL \_ Zeichnen des \_ Pixel Tokens \_ Vertex- \| \_ \_ Pixel \_ Token-Vertex kopieren

PassThru < GL- \_ Pass- \_ through- \_ Tokenwert

Vertex < 2D \| 3D- \| 3dcolor \| 3dcolortexture \| 4dcolortexture

2D-Wert für < Wert

Wert des 3D--< Werts

3dcolor-< Wert Wert Farbe

3dcolortexture < Werte Wert farbtex

4dcolortexture < Werte Wert farbtex

Farbe < RGBA- \| Index

Wert des RGBA-< Wert Werts

Index < Wert

Wert Wert Wert des Tex-< Werts

Der *value* -Parameter ist eine Gleit Komma Zahl, und *n* ist eine Gleit Komma Zahl, die die Anzahl der Scheitel Punkte im Polygon gibt. Im folgenden finden Sie symbolische Gleit Komma Konstanten: GL- \_ Punkt \_ Token, GL- \_ Zeilen \_ Token, GL \_ -Zeilen Zurücksetzungs \_ \_ Token, GL- \_ Polygon- \_ Token, GL- \_ \_ bitmaptoken, GL \_ \_ -Pixel Token, GL \_ \_ \_ -Kopier Pixel \_ Token und GL- \_ Pass-Through- \_ \_ Token. \_ \_ Das Token zum Zurücksetzen von GL \_ wird zurückgegeben, wenn das Zeilen stippingmuster zurückgesetzt wird. Die als Scheitel Punkte zurückgegebenen Daten sind vom *Feedtyp* abhängig.

In der folgenden Tabelle ist die Entsprechung zwischen *Typ* und Anzahl der Werte pro Scheitelpunkt *k* ist 1 im Farb Index Modus und 4 im RGBA-Modus.



| type                   | Koordinaten        | Color | Struktur | Gesamtzahl der Werte |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| GL \_ 3D- \_ Farbe          | *x*, *y*, *z*      | *km*   |         | 3 + *k*                |
| GL \_ 3D- \_ Farb \_ Textur | *x*, *y*, *z*,     | *km*   | 4       | 7 + *k*                |
| GL \_ 4D \_ Farb \_ Textur | *x*, *y*, *z*, *w* | *km*   | 4       | 8 + *k*                |



 

Feedback-vertexkoordinaten befinden sich in Fenster Koordinaten, mit Ausnahme von " *w*", die sich in Clip Koordinaten befinden. Die Farben des Feedbacks werden beleuchtet, wenn Beleuchtung aktiviert ist. Es werden Feedback Texturkoordinaten generiert, wenn die Generierung der Textur Koordinate aktiviert ist. Sie werden immer von der Textur Matrix transformiert.

Die **glfeedbackbuffer** -Funktion wird, wenn Sie in einer Anzeigeliste verwendet wird, nicht in die Anzeigeliste kompiliert, sondern wird sofort ausgeführt.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glfeedbackbuffer** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gllinestippel**](gllinestipple.md)
</dt> <dt>

[**glpassthrough**](glpassthrough.md)
</dt> <dt>

[**glpolygonmode**](glpolygonmode.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> <dt>

[**glselectbuffer**](glselectbuffer.md)
</dt> </dl>

 

 





