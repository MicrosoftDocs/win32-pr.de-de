---
title: glMap2f-Funktion (Gl.h)
description: Die glMap2f-Funktion definiert eine zweidimensionale Auswertung. | glMap2f-Funktion (Gl.h)
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
ms.openlocfilehash: fb9f0d33cea662f35cdbbfb0b414d0254883cd619d55832550abdec3668ef070
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741380"
---
# <a name="glmap2f-function"></a>glMap2f-Funktion

Die [**Funktionen glMap2d**](glmap2d.md) und **glMap2f** definieren eine zweidimensionale Auswertung.

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
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 3**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die *x, y und* *z darstellen.* Interne [**glVertex3-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 4**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die *x, y, z und* *w darstellen.* Interne [**glVertex4-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ MAP2 \_ INDEX**</dt> </dl>                                 | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der einen Farbindex darstellt. Interne [**glIndex-Befehle**](glindex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Index wird jedoch nicht mit dem Wert dieser **glIndex-Befehle** aktualisiert.<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                          | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die Rot, Grün, Blau und Alpha darstellen. Interne [**glColor4-Befehle**](glcolor-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Farbe wird jedoch nicht mit dem Wert dieser **glColor4-Befehle** aktualisiert.<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                              | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die *x-, y-* und *z-Komponenten* eines normalen Vektors darstellen. Interne [**glNormal-Befehle**](glnormal-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Normalwert wird jedoch nicht mit dem Wert dieser **glNormal-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der die *Texturkoordinate* darstellt. Interne [**glTexCoord1-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Jeder Kontrollpunkt besteht aus zwei Gleitkommawerten, die die *Texturkoordinaten s* und *t* darstellen. Interne [**glTexCoord2-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die *Texturkoordinaten s, t* und *r* darstellen. Interne [**glTexCoord3-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die die *Texturkoordinaten s, t, r* *und q* darstellen. Interne [**glTexCoord4-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *u*^, einer der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet werden.

</dd> <dt>

*u2* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *u*^, einer der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet werden.

</dd> <dt>

*ustride* 
</dt> <dd>

Die Anzahl der Gleitkommazahlen oder Doubles zwischen dem Anfang des Kontrollpunkts **R** *ij* und dem Anfang des Kontrollpunkts **R** <sub>(i\ +1\ )\ j</sub>, wobei *i* und *j* die Indizes für den *u-* bzw. *v-Kontrollpunkt* sind. Dadurch können Steuerungspunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung ist, dass die Werte für einen bestimmten Kontrollpunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*uorder* 
</dt> <dd>

Die Dimension des Kontrollpunktarrays auf der *u-Achse.* Muss positiv sein.

</dd> <dt>

*v1* 
</dt> <dd>

Eine lineare Zuordnung von *v*, wie [**glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *v*^, einer der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet werden.

</dd> <dt>

*v2* 
</dt> <dd>

Eine lineare Zuordnung von *v*, wie [**glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *v*^, einer der beiden Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet werden.

</dd> <dt>

*vstride* 
</dt> <dd>

Die Anzahl der Gleitkommazahlen oder Doubles zwischen dem Anfang des Kontrollpunkts **R** *ij* und dem Anfang des Kontrollpunkts **R** <sub>i(j\ +1\ ),</sub>wobei *i* und *j* die Indizes für den *u-* bzw. *v-Kontrollpunkt* sind. Dadurch können Steuerungspunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung ist, dass die Werte für einen bestimmten Kontrollpunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*vorder* 
</dt> <dd>

Die Dimension des Kontrollpunktarrays auf der *v-Achse.* Muss positiv sein.

</dd> <dt>

*Punkte* 
</dt> <dd>

Ein Zeiger auf das Array von Kontrollpunkten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *u1* war gleich *u2,* oder *v1* war gleich *v2.*<br/>                                                                         |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *ustride* oder *vstride* war kleiner als die Anzahl der Werte in einem Kontrollpunkt.<br/>                                       |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *uorder oder* *vorder* war kleiner als eins oder GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                     |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Auswertungen bieten eine Möglichkeit, polynomiale oder rationale polynomiale Zuordnung zu verwenden, um Scheitelungen, Normals, Texturkoordinaten und Farben zu erzeugen. Die von einer Auswertung erzeugten Werte werden an weitere Phasen der OpenGL-Verarbeitung gesendet, als ob sie mithilfe der Befehle [**glVertex,**](glvertex-functions.md) [**glNormal,**](glnormal-functions.md) [**glTexCoord**](gltexcoord-functions.md)und [**glColor**](glcolor-functions.md) dargestellt worden wäre, mit der Ausnahme, dass die generierten Werte die aktuelle Normal- oder Texturkoordinate oder Farbe nicht aktualisieren.

Alle polynomialen oder rationalen polynomialen Splines eines beliebigen Grads (bis zu dem von der OpenGL-Implementierung unterstützten maximalen Grad) können mithilfe von Auswertungen beschrieben werden. Dazu gehören fast alle Oberflächen, die in Computergrafiken verwendet werden, einschließlich B-Spline-Oberflächen, NURBS-Oberflächen, Bézieroberflächen und so weiter.

Auswerter definieren Oberflächen basierend auf bivariaten Polynomen. Definieren **Sie p** (*u*^,*v*^) als

![Gleichung, die die Definition von p () zeigt.](images/map05.png)

wobei **R** *ij* ein Kontrollpunkt ist, () ist das ith-Polynom von Grade 

*n* (*uorder*  =  *n* + 1)

![Gleichung, die die Polynomie des Grads n zeigt.](images/map06.png)

und () ist das j-th-Polynom von Degree *m* (*vorder*   =  *m* + 1)

![Gleichung, die die Polynomie Von Grad m zeigt.](images/map07.png)

Denken Sie daran, dass

![Gleichungen mit Äquivalenz zu 1.](images/map08.png)

Die **glMap2-Funktion** wird verwendet, um die Basis zu definieren und anzugeben, welche Art von Werten erzeugt werden. Nach der Definition kann eine Zuordnung aktiviert und deaktiviert werden, indem [**glEnable**](glenable.md) und **glDisable** mit dem Kartennamen , einem der neun vordefinierten Werte für das *Ziel,* wie oben beschrieben, aufruft. Wenn [**glEvalCoord2**](glevalcoord-functions.md) die Werte *u* und *v* präsentiert, werden die bivariaten Polynomen Von Der Polynomen werden mit *u*^ und *v*^ausgewertet, wobei

![Die Gleichung zeigt die Definition Von Ihnen^.](images/map09.png)

und

![Gleichung, die die Definition von v^ zeigt.](images/map10.png)

Der *Zielparameter* ist eine symbolische Konstante, die angibt, welche Art von Kontrollpunkten *in* Punkten bereitgestellt werden und welche Ausgabe generiert wird, wenn die Karte ausgewertet wird.

Die *Parameter ustride,* *uorder,* *vstride,* *vorder* und *points* definieren die Arrayadrierung für den Zugriff auf die Kontrollpunkte. Der *Points-Parameter* ist die Position des ersten Kontrollpunkts, der je nachdem, welche Zuordnung definiert wird, einen, zwei, drei oder vier zusammenhängende Speicherorte einnimmt. Das Array *enthält uorder* x *vordere* Kontrollpunkte. Der *ustride-Parameter* gibt an, wie viele Gleitkomma- oder double-Positionen übersprungen werden, um den internen Speicherzeiger vom Steuerungspunkt **R** *ij* auf den Steuerungspunkt **R** <sub>(\ i+1\ )j</sub>zu bringen. Der *vstride-Parameter* gibt an, wie viele float- oder double-Positionen übersprungen werden, um den internen Speicherzeiger vom Steuerungspunkt **R** *ij* auf den Kontrollpunkt **R**<sub>i(j\ +1\ )</sub>zu verbessern.

Wie bei allen OpenGL-Befehlen, die Zeiger auf Daten akzeptieren,  ist dies so, als ob der Inhalt der Punkte von **glMap2** kopiert wurde, bevor er zurückgegeben wurde. Änderungen am Inhalt von Punkten *haben* keine Auswirkungen, nachdem **glMap2** aufgerufen wurde.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMap2 ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ MAP2 \_ VERTEX \_ 3

**glIsEnabled mit** Argument GL \_ MAP2 \_ VERTEX \_ 4

**glIsEnabled mit** Argument GL \_ MAP2 \_ INDEX

**glIsEnabled mit Argument** GL \_ MAP2 COLOR \_ \_ 4

**glIsEnabled mit** Argument GL \_ MAP2 \_ NORMAL

**glIsEnabled mit Argument** GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1

**glIsEnabled mit Argument** GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2

**glIsEnabled mit Argument** GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3

**glIsEnabled mit Argument** GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





