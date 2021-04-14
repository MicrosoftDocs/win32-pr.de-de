---
title: glMap1f-Funktion (Gl.h)
description: Die glMap1f-Funktion definiert eine eindimensionale Auswertung. | glMap1f-Funktion (GL. h)
ms.assetid: c016ad80-b507-4e21-829f-f173d5c8dee6
keywords:
- glMap1f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMap1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafcbfc40b3359cd8faa6f52f6635c1c86f03f17
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104565445"
---
# <a name="glmap1f-function"></a>glMap1f-Funktion

Die [**glMap1d**](glmap1d.md) -Funktion und die **glMap1f** -Funktion definieren einen eindimensionalen Evaluator.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMap1f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   stride,
         GLint   order,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Art der Werte, die von der Auswertung generiert werden. Symbolische Konstanten. Der *Ziel* Parameter ist eine symbolische Konstante, die angibt, welche Art von Kontrollpunkten in *Punkten* bereitgestellt werden und welche Ausgabe generiert wird, wenn die Zuordnung ausgewertet wird. Es kann einen von neun vordefinierten Werten annehmen.



| Wert                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ zuordnung1 \_ Scheitelpunkt \_ 3**</dt> </dl>                       | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die *x, y* und *z* darstellen. Interne [**glVertex3**](glvertex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Scheitelpunkt \_ 4**</dt> </dl>                       | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die *x, y, z* und *w* darstellen. Interne [**glVertex4**](glvertex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ zuordnung1 \_ Index**</dt> </dl>                                 | Jeder Kontrollpunkt ist ein einzelner Gleit Komma Wert, der einen Farbindex darstellt. Interne [**glindex**](glindex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Index wird jedoch nicht mit dem Wert dieser **glindex** -Befehle aktualisiert.<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Farbe \_ 4**</dt> </dl>                          | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die rot, grün, blau und Alpha darstellen. Interne [**glColor4**](glcolor-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Farbe wird jedoch nicht mit dem Wert dieser **glColor4** -Befehle aktualisiert.<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ zuordnung1 \_ Normal**</dt> </dl>                              | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die die *x-, y* -und *z* -Komponenten eines normalen Vektors darstellen. Interne [**glnormal**](glnormal-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Normalwert wird jedoch nicht mit dem Wert dieser **glnormal** -Befehle aktualisiert.<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur \_ Koord \_ 1**</dt> </dl> | Jeder Kontrollpunkt ist ein einzelner Gleit Komma Wert, der die *s* -Textur Koordinate darstellt. Interne [**glTexCoord1**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur- \_ Koord \_ 2**</dt> </dl> | Jeder Kontrollpunkt ist zwei Gleit Komma Werte, die die *s* -und *t* -Texturkoordinaten darstellen. Interne [**glTexCoord2**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur \_ Koord \_ 3**</dt> </dl> | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die die Texturkoordinaten *s, t* und *r* darstellen. Interne [**glTexCoord3**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ zuordnung1 \_ Textur- \_ Koord \_ 4**</dt> </dl> | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die die Texturkoordinaten " *s", "t* ", "r" und " *q* " darstellen. Interne [**glTexCoord4**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Eine lineare Zuordnung von *u*(wie [**glEvalCoord1**](glevalcoord-functions.md)) zu *u*^, der Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*hinweg* 
</dt> <dd>

Eine lineare Zuordnung von *u*(wie [**glEvalCoord1**](glevalcoord-functions.md)) zu *u*^, der Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*Schritt* 
</dt> <dd>

Die Anzahl der Gleit Komma Zahlen oder Doppelpunkte zwischen dem Anfang eines Steuerungs Punkts und dem Anfang der nächsten in der Datenstruktur, auf die in *Points* verwiesen wird. Dadurch können Kontrollpunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung besteht darin, dass die Werte für einen bestimmten Steuerungspunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*order* 
</dt> <dd>

Die Anzahl der Kontrollpunkte. Muss positiv sein.

</dd> <dt>

*Punkte* 
</dt> <dd>

Ein Zeiger auf das Array von Steuerungs Punkten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *U1* war gleich *U2*.<br/>                                                                                                    |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | der *Stride* -Wert war kleiner als die Anzahl der Werte in einem Steuerungspunkt.<br/>                                                            |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Reihen* Folge war kleiner als 1 oder GL \_ Max \_ eval \_ .<br/>                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Evaluatoren bieten eine Möglichkeit, Polynoms-oder rational Polynoms-Mapping zu verwenden, um Vertices, normale, Texturkoordinaten und Farben zu erstellen. Die Werte, die von einem Auswertung erzeugt werden, werden an weitere Phasen der OpenGL-Verarbeitung gesendet, so als wären Sie mit den Befehlen " [**glVertex**](glvertex-functions.md)", " [**glnormal**](glnormal-functions.md)", " [**gltexcoord**](gltexcoord-functions.md)" und " [**glcolor**](glcolor-functions.md) " dargestellt worden, mit der Ausnahme, dass die generierten Werte nicht die aktuellen normalen, Texturkoordinaten oder Farben aktualisieren

Alle polynomialen oder rationalen polynomialen Splines (bis zu dem maximalen Grad, der von der OpenGL-Implementierung unterstützt wird) können mithilfe von auswergratoren beschrieben werden. Dazu zählen fast alle in Computergrafiken verwendeten Splines, einschließlich B-Splines, Bezier-Kurven, Hermite-Splines usw.

Evaluatoren definieren Kurven auf der Grundlage von Bernstein Polynomen. Definieren von **p** () als

![Gleichung, die die Definition von p () anzeigt.](images/map01.png)

Dabei ist **R**_i_ ein Steuerungspunkt, und () ist *der Bernstein* polynommial von Grad *n* (*Reihenfolge*  = *n* + 1):

![Gleichung, die den Bernstein Polynoms von Grad n anzeigt.](images/map02.png)

Beachten Sie, dass

![Gleichungen, die Äquivalenz zu 1 darstellen.](images/map03.png)

Die **glMap1** -Funktion wird verwendet, um die Basis zu definieren und anzugeben, welche Art von Werten erstellt wird. Nachdem Sie definiert wurde, kann eine Zuordnung aktiviert und deaktiviert werden, indem [**glEnable**](glenable.md) und **glEnable** mit dem Zuordnungs Namen aufgerufen wird. Dies ist einer der neun vordefinierten Werte für das oben beschriebene *Ziel* . Die [glEvalCoord1](glevalcoord-functions.md) -Funktion wertet die eindimensionalen Zuordnungen aus, die aktiviert sind. Wenn **glEvalCoord1** den Wert *u* darstellt, werden die Bernstein Funktionen mit *u*^ ausgewertet, wobei

![Gleichung, die die Definition von Ihnen ^ anzeigt.](images/map04.png)

Die Parameter *Stride*, *Order* und *Points* definieren die Array Adressierung für den Zugriff auf die Steuerpunkte. Der *Points* -Parameter ist der Speicherort des ersten Kontroll Punkts, der einen, zwei, drei oder vier zusammenhängende Speicherorte einnimmt, je nachdem, welche Zuordnung definiert wird. Der *Order* -Parameter entspricht der Anzahl von Steuerungs Punkten im Array. Der *Stride* -Parameter gibt an, wie viele float-oder Double-Speicherorte den internen Speicher Zeiger zum Erreichen des nächsten Steuerungs Punkts verschieben.

Wie bei allen OpenGL-Befehlen, die Zeiger auf Daten akzeptieren, ist es so, als ob der Inhalt der *Punkte* vor der Rückgabe von **glMap1** kopiert wurde. Änderungen am Inhalt von *Punkten* haben keine Auswirkung, nachdem **glMap1** aufgerufen wurde.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMap1** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max \_ eval \_ Order

[**glgetmap**](glgetmap.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 3

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 4

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Index

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Farbe \_ 4

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Normal

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 1

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 2

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 3

**glisenabled** mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 4

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

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[**glevalmesh**](glevalmesh-functions.md)
</dt> <dt>

[**glevalpoint**](glevalpoint.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glmapgrid**](glmapgrid-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





