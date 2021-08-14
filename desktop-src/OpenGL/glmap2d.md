---
title: glMap2d-Funktion (Gl.h)
description: Die glMap2d-Funktion definiert eine zweidimensionale Auswertung. | glMap2d-Funktion (Gl.h)
ms.assetid: d8645d19-bec1-4efd-a657-6e7d52d706a9
keywords:
- glMap2d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMap2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c86699f3d1a897476b33d15aec857228c6293d9bd66e260528cdaf468d664252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359043"
---
# <a name="glmap2d-function"></a>glMap2d-Funktion

Die Funktionen **glMap2d** und [**glMap2f**](glmap2f.md) definieren eine zweidimensionale Auswertung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMap2d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    ustride,
         GLint    uorder,
         GLdouble v1,
         GLdouble v2,
         GLint    vstride,
         GLint    vorder,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Art von Werten, die von der Auswertung generiert werden. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 3**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die *x, y* und *z* darstellen. Interne [**glVertex3-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 4**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die *x, y, z* und *w* darstellen. Interne [**glVertex4-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ MAP2 \_ INDEX**</dt> </dl>                                 | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der einen Farbindex darstellt. Interne [**glIndex-Befehle**](glindex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Index wird jedoch nicht mit dem Wert dieser **glIndex-Befehle** aktualisiert.<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                          | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die Rot, Grün, Blau und Alpha darstellen. Interne [**glColor4-Befehle**](glcolor-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Farbe wird jedoch nicht mit dem Wert dieser **glColor4-Befehle** aktualisiert.<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                              | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die *x-, y-* und *z-Komponenten* eines normalen Vektors darstellen. Interne [**glNormal-Befehle**](glnormal-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Normalität wird jedoch nicht mit dem Wert dieser **glNormal-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der die *Texturkoordinate* darstellt. Interne [**glTexCoord1-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Jeder Kontrollpunkt besteht aus zwei Gleitkommawerten, die die Texturkoordinaten *s* und *t* darstellen. Interne [**glTexCoord2-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die Texturkoordinaten *s, t* und *r* darstellen. Interne [**glTexCoord3-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die die Texturkoordinaten *s, t, r* und *q* darstellen. Interne [**glTexCoord4-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**in glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *u*^, einer der beiden Variablen, die von den von diesem Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*u2* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**in glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *u*^, einer der beiden Variablen, die von den von diesem Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*ustride* 
</dt> <dd>

Die Anzahl von Gleitkommazahlen oder Doubles zwischen dem Anfang des Kontrollpunkts **R** *ij* und dem Anfang des Kontrollpunkts **R** <sub>(i\ +1\ )\j,</sub>wobei *i* und *j* die *u-* bzw. *v-Steuerungspunktindizes* sind. Dadurch können Steuerpunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung besteht darin, dass die Werte für einen bestimmten Steuerungspunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*uorder* 
</dt> <dd>

Die Dimension des Steuerelementpunktarrays auf der *u-Achse.* Muss positiv sein.

</dd> <dt>

*v1* 
</dt> <dd>

Eine lineare Zuordnung von *v*, wie [**für glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *v*^, einer der beiden Variablen, die von den von diesem Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*v2* 
</dt> <dd>

Eine lineare Zuordnung von *v*, wie [**für glEvalCoord2**](glevalcoord-functions.md)dargestellt, zu *v*^, einer der beiden Variablen, die von den von diesem Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*vstride* 
</dt> <dd>

Die Anzahl von Gleitkommazahlen oder Doubles zwischen dem Anfang des Kontrollpunkts **R** *ij* und dem Anfang des Kontrollpunkts **R** <sub>i(j\ +1\ )</sub>, wobei *i* und *j* die *u-* bzw. v-Steuerungspunktindizes sind.  Dadurch können Steuerpunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung besteht darin, dass die Werte für einen bestimmten Steuerungspunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*vorder* 
</dt> <dd>

Die Dimension des Steuerelementpunktarrays auf der *v-Achse.* Muss positiv sein.

</dd> <dt>

*Punkte* 
</dt> <dd>

Ein Zeiger auf das Array von Steuerelementpunkten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *u1* war gleich *u2,* oder *v1* war gleich *v2*.<br/>                                                                         |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *ustride* oder *vstride* war kleiner als die Anzahl der Werte in einem Kontrollpunkt.<br/>                                       |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Entweder *uorder* oder *vorder* war kleiner als 1 oder GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                     |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Auswertungen bieten eine Möglichkeit, polynomiale oder rationale Polynomzuordnungen zu verwenden, um Scheitelpunkte, Normalwerte, Texturkoordinaten und Farben zu erzeugen. Die von einer Auswertung erzeugten Werte werden an weitere Phasen der OpenGL-Verarbeitung gesendet, so als wären sie mit den Befehlen [**glVertex,**](glvertex-functions.md) [**glNormal,**](glnormal-functions.md) [**glTexCoord**](gltexcoord-functions.md)und [**glColor**](glcolor-functions.md) dargestellt worden, außer dass die generierten Werte die aktuelle Normalität, Texturkoordinaten oder Farbe nicht aktualisieren.

Alle polynomialen oder rationalen polynomialen Splines eines beliebigen Grads (bis zu dem von der OpenGL-Implementierung unterstützten maximalen Grad) können mithilfe von Auswertungen beschrieben werden. Dazu gehören fast alle Oberflächen, die in Computergrafiken verwendet werden, einschließlich B-Spline-Oberflächen, NURBS-Oberflächen, Bézieroberflächen usw.

Auswertungen definieren Oberflächen, die auf bivariaten Polynomen basieren. Definieren Sie **p** (*u*^,*v*^) als

![Gleichung, die die Definition von p () zeigt.](images/map05.png)

dabei ist **R** *ij* ein Kontrollpunkt, () ist das *i* th Polynomial des Schweregrads

*n* (*uorder*  =  *n* + 1)

![Gleichung, die die Polynomiale "Grade n" zeigt.](images/map06.png)

und () ist das *polynomiale* Polynom j th Von Grad *m* (*vorder*  =  *m* + 1)

![Gleichung, die die Polynomialintepolynom von Degree m zeigt.](images/map07.png)

Denken Sie daran, dass

![Gleichungen mit Äquivalenz zu 1.](images/map08.png)

Die **glMap2-Funktion** wird verwendet, um die Basis zu definieren und anzugeben, welche Art von Werten erzeugt werden. Nach der Definition kann eine Zuordnung aktiviert und deaktiviert werden, indem [**glEnable**](glenable.md) und **glDisable** mit dem Kartennamen , einem der neun vordefinierten Werte für das *Ziel,* wie oben beschrieben, aufruft. Wenn [**glEvalCoord2**](glevalcoord-functions.md) die Werte *u* und *v* präsentiert, werden die bivariaten Polynomen Von Der Polynomen werden mit *u*^ und *v*^ausgewertet, wobei

![Die Gleichung zeigt die Definition Von Ihnen^.](images/map09.png)

und

![Die Gleichung zeigt die Definition von v^.](images/map10.png)

Der *Zielparameter* ist eine symbolische Konstante, die angibt, welche Art von Kontrollpunkten *in* Punkten bereitgestellt werden und welche Ausgabe generiert wird, wenn die Karte ausgewertet wird.

Die *Parameter ustride,* *uorder,* *vstride,* *vorder* und *points* definieren die Arrayadrierung für den Zugriff auf die Kontrollpunkte. Der *Points-Parameter* ist die Position des ersten Kontrollpunkts, der je nachdem, welche Zuordnung definiert wird, einen, zwei, drei oder vier zusammenhängende Speicherorte einnimmt. Das Array *enthält uorder* x *vordere* Kontrollpunkte. Der *ustride-Parameter* gibt an, wie viele Gleitkomma- oder double-Positionen übersprungen werden, um den internen Speicherzeiger vom Steuerungspunkt **R** *ij* auf den Steuerungspunkt **R** <sub>(\ i+1\ )j</sub>zu bringen. Der *vstride-Parameter* gibt an, wie viele float- oder double-Positionen übersprungen werden, um den internen Speicherzeiger vom Steuerungspunkt **R** *ij* auf den Kontrollpunkt **R**<sub>i(j\ +1\ )</sub>zu verbessern.

Wie bei allen OpenGL-Befehlen, die Zeiger auf Daten akzeptieren,  ist dies so, als ob der Inhalt der Punkte vor der Rückkehr von **glMap2** kopiert worden wäre. Änderungen am Inhalt von Punkten *haben* keine Auswirkungen, nachdem **glMap2** aufgerufen wurde.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMap2 ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ MAP2 \_ VERTEX \_ 3

**glIsEnabled mit** Argument GL \_ MAP2 \_ VERTEX \_ 4

**glIsEnabled mit** Argument GL \_ MAP2 \_ INDEX

**glIsEnabled mit** Argument GL \_ MAP2 \_ COLOR \_ 4

**glIsEnabled mit Argument** GL \_ MAP2 \_ NORMAL

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

 

 





