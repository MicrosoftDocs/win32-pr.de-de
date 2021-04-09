---
title: glMap2f-Funktion (Gl.h)
description: Die glMap2f-Funktion definiert eine zweidimensionale Auswertung. | glMap2f-Funktion (GL. h)
ms.assetid: 804fbf65-98a8-41af-8c39-5b83f3d341b0
keywords:
- glMap2f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMap2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152183ced46b55bcdf2038399583c1ecac8c5678
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869715"
---
# <a name="glmap2f-function"></a>glMap2f-Funktion

Die [**glMap2d**](glmap2d.md) -Funktion und die **glMap2f** -Funktion definieren einen zweidimensionalen Evaluator.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMap2f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   ustride,
         GLint   uorder,
         GLfloat v1,
         GLfloat v2,
         GLint   vstride,
         GLint   vorder,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Art der Werte, die von der Auswertung generiert werden. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ map2 \_ Scheitelpunkt \_ 3**</dt> </dl>                       | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die *x, y* und *z* darstellen. Interne [**glVertex3**](glvertex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ map2 \_ Scheitelpunkt \_ 4**</dt> </dl>                       | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die *x, y, z* und *w* darstellen. Interne [**glVertex4**](glvertex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ map2 \_ Index**</dt> </dl>                                 | Jeder Kontrollpunkt ist ein einzelner Gleit Komma Wert, der einen Farbindex darstellt. Interne [**glindex**](glindex-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Index wird jedoch nicht mit dem Wert dieser **glindex** -Befehle aktualisiert.<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ map2 \_ Farbe \_ 4**</dt> </dl>                          | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die rot, grün, blau und Alpha darstellen. Interne [**glColor4**](glcolor-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Farbe wird jedoch nicht mit dem Wert dieser **glColor4** -Befehle aktualisiert.<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ map2 \_ Normal**</dt> </dl>                              | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die die *x-, y* -und *z* -Komponenten eines normalen Vektors darstellen. Interne [**glnormal**](glnormal-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Normalwert wird jedoch nicht mit dem Wert dieser **glnormal** -Befehle aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ map2 \_ Textur \_ Koord \_ 1**</dt> </dl> | Jeder Kontrollpunkt ist ein einzelner Gleit Komma Wert, der die *s* -Textur Koordinate darstellt. Interne [**glTexCoord1**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ map2 \_ Textur- \_ Koord \_ 2**</dt> </dl> | Jeder Kontrollpunkt ist zwei Gleit Komma Werte, die die *s* -und *t* -Texturkoordinaten darstellen. Interne [**glTexCoord2**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ map2 \_ Textur \_ Koord \_ 3**</dt> </dl> | Jeder Kontrollpunkt ist drei Gleit Komma Werte, die die Texturkoordinaten *s, t* und *r* darstellen. Interne [**glTexCoord3**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ map2 \_ Textur- \_ Koord \_ 4**</dt> </dl> | Jeder Kontrollpunkt ist vier Gleit Komma Werte, die die Texturkoordinaten " *s", "t* ", "r" und " *q* " darstellen. Interne [**glTexCoord4**](gltexcoord-functions.md) -Befehle werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **gltexcoord** -Befehle aktualisiert.<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Eine lineare Zuordnung von *u*(wie [**glEvalCoord2**](glevalcoord-functions.md)) zu *u*^, eine der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*hinweg* 
</dt> <dd>

Eine lineare Zuordnung von *u*(wie [**glEvalCoord2**](glevalcoord-functions.md)) zu *u*^, eine der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*ustride* 
</dt> <dd>

Die Anzahl von Gleit Komma Zahlen oder Doppelpunkten zwischen dem Anfang des Steuerungs Punkts **r** *IJ* und dem Anfang des Steuerungs Punkts **r** <sub>(i \ + 1 \) \ j</sub>, wobei *i* und *j* *die Index-bzw* . *v* -Steuerungspunkt Indizes sind. Dadurch können Kontrollpunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung besteht darin, dass die Werte für einen bestimmten Steuerungspunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*uorder* 
</dt> <dd>

Die Dimension des Steuerungspunkt Arrays in der *u*-Achse. Muss positiv sein.

</dd> <dt>

*v1* 
</dt> <dd>

Eine lineare Zuordnung von *v*(wie [**glEvalCoord2**](glevalcoord-functions.md)) zu *v*^, eine der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*v2* 
</dt> <dd>

Eine lineare Zuordnung von *v*(wie [**glEvalCoord2**](glevalcoord-functions.md)) zu *v*^, eine der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*vstride* 
</dt> <dd>

Die Anzahl von Gleit Komma Zahlen oder Doppelpunkten zwischen dem Anfang des Steuerungs Punkts **r** *IJ* und dem Anfang des Steuerungs Punkts **r** <sub>i (j \ + 1 \)</sub>, wobei *i* und *j* *die Index Index-bzw* . *v* -Steuerungspunkt Indizes sind. Dadurch können Kontrollpunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung besteht darin, dass die Werte für einen bestimmten Steuerungspunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*HI* 
</dt> <dd>

Die Dimension des Steuerungspunkt Arrays in der *v*-Achse. Muss positiv sein.

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
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *U1* war gleich *U2*, oder *v1* war gleich *v2*.<br/>                                                                         |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Ustride* oder *vstride* war kleiner als die Anzahl der Werte in einem Kontrollpunkt.<br/>                                       |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Entweder *uorder* oder *Vorder* ist kleiner als 1 oder GL \_ Max \_ eval \_ Order.<br/>                                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Evaluatoren bieten eine Möglichkeit, Polynoms-oder rational Polynoms-Mapping zu verwenden, um Vertices, normale, Texturkoordinaten und Farben zu erstellen. Die Werte, die von einem Auswertung erzeugt werden, werden an weitere Phasen der OpenGL-Verarbeitung gesendet, so als wären Sie mit den Befehlen " [**glVertex**](glvertex-functions.md)", " [**glnormal**](glnormal-functions.md)", " [**gltexcoord**](gltexcoord-functions.md)" und " [**glcolor**](glcolor-functions.md) " dargestellt worden, mit dem Unterschied, dass die generierten Werte die aktuellen normalen, Texturkoordinaten oder Farben nicht aktualisieren.

Alle polynomialen oder rationalen polynomialen Splines (bis zu dem maximalen Grad, der von der OpenGL-Implementierung unterstützt wird) können mithilfe von auswergratoren beschrieben werden. Dazu zählen fast alle in Computergrafiken verwendeten Oberflächen, einschließlich B-Spline-Oberflächen, NURBS-Oberflächen, Bezier-Oberflächen usw.

Evaluatoren definieren Oberflächen auf der Grundlage von Bivariate Bernstein Polynomen. Definieren von **p** (*u*^,*v*^) als

![Gleichung, die die Definition von p () anzeigt.](images/map05.png)

wobei **R** *IJ* ein Kontrollpunkt ist, () ist die *i* Th Bernstein Polynoms of Degree

*n* (*uorder*  =  *n* + 1)

![Gleichung, die den Bernstein Polynoms von Grad n anzeigt.](images/map06.png)

and () ist die *j* Th Bernstein Polynoms of Degree *m* (*Vorder*  =  *m* + 1)

![Gleichung, die den Bernstein Polynoms von Grad m anzeigt.](images/map07.png)

Beachten Sie, dass

![Gleichungen, die Äquivalenz zu 1 darstellen.](images/map08.png)

Die **glMap2** -Funktion wird verwendet, um die Basis zu definieren und anzugeben, welche Art von Werten erstellt wird. Nach der Definition kann eine Zuordnung aktiviert und deaktiviert werden, indem Sie [**glEnable**](glenable.md) aufrufen **und mit dem** Zuordnungs Namen einen der neun vordefinierten Werte für *target*(oben beschrieben) aufrufen. Wenn [**glEvalCoord2**](glevalcoord-functions.md) die Werte *u* und *v* anzeigt, werden die Bivariate Bernstein Polynomen mithilfe von *u*^ und *v*^ ausgewertet, wobei

![Gleichung, die die Definition von Ihnen ^ anzeigt.](images/map09.png)

und

![Gleichung, die die Definition von v ^ anzeigt.](images/map10.png)

Der *Ziel* Parameter ist eine symbolische Konstante, die angibt, welche Art von Kontrollpunkten in *Punkten* bereitgestellt werden und welche Ausgabe generiert wird, wenn die Zuordnung ausgewertet wird.

Die Parameter *ustride*, *uorder*, *vstride*, *Vorder* und *Points* definieren die Array Adressierung für den Zugriff auf die Steuerpunkte. Der *Points* -Parameter ist der Speicherort des ersten Kontroll Punkts, der einen, zwei, drei oder vier zusammenhängende Speicherorte einnimmt, je nachdem, welche Zuordnung definiert wird. Es sind *uorder* x *Vorder* Steuerungs Punkte im Array vorhanden. Der *ustride* -Parameter gibt an, wie viele float-oder Double-Positionen übersprungen werden, um den internen Speicher Zeiger von Steuerungspunkt **r** *IJ* auf Steuerungspunkt **r** <sub>(\ i + 1 \) j</sub>zu verschieben. Der *vstride* -Parameter gibt an, wie viele float-oder Double-Positionen übersprungen werden, um den internen Speicher Zeiger von Steuerungspunkt **r** *IJ* auf Steuerungspunkt **r**<sub>i (j \ + 1 \)</sub>zu verschieben.

Wie bei allen OpenGL-Befehlen, die Zeiger auf Daten akzeptieren, ist es so, als ob der Inhalt der *Punkte* vor der Rückgabe von **glMap2** kopiert wurde. Änderungen am Inhalt von *Punkten* haben keine Auswirkung, nachdem **glMap2** aufgerufen wurde.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMap2** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max \_ eval \_ Order

[**glgetmap**](glgetmap.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 3

**glisenabled** mit dem Argument GL \_ map2 \_ Vertex \_ 4

**glisenabled** mit dem Argument GL \_ map2 \_ Index

**glisenabled** mit dem Argument GL \_ map2 \_ Farbe \_ 4

**glisenabled** mit dem Argument GL \_ map2 \_ Normal

**glisenabled** mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 1

**glisenabled** mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 2

**glisenabled** mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 3

**glisenabled** mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 4

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

[**glMap1**](glmap1.md)
</dt> <dt>

[**glmapgrid**](glmapgrid-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





