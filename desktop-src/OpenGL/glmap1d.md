---
title: glMap1d-Funktion (Gl.h)
description: Die glMap1d-Funktion definiert eine eindimensionale Auswertung. | glMap1d-Funktion (Gl.h)
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- glMap1d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f1d17312cae14da955641d0009235a45fa23e65a3a04e35f692a4bb5418722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520430"
---
# <a name="glmap1d-function"></a>glMap1d-Funktion

Die **Funktionen glMap1d** und [**glMap1f**](glmap1f.md) definieren eine eindimensionale Auswertung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Art der Werte, die von der Auswertung generiert werden. Symbolische Konstanten. Der *Zielparameter* ist eine symbolische Konstante, die angibt, welche Art von Kontrollpunkten *in* Punkten bereitgestellt werden und welche Ausgabe generiert wird, wenn die Karte ausgewertet wird. Es kann einer von neun vordefinierten Werten angenommen werden.



| Wert                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 3**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die *x, y und* *z darstellen.* Interne [**glVertex3-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 4**</dt> </dl>                       | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die *x, y, z und* *w darstellen.* Interne [**glVertex4-Befehle**](glvertex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ INDEX**</dt> </dl>                                 | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der einen Farbindex darstellt. Interne [**glIndex-Befehle**](glindex-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Der aktuelle Index wird jedoch nicht mit dem Wert dieser **glIndex-Befehle** aktualisiert.<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COLOR \_ 4**</dt> </dl>                          | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die Rot, Grün, Blau und Alpha darstellen. Interne [**glColor4-Befehle**](glcolor-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Farbe wird jedoch nicht mit dem Wert dieser **glColor4-Befehle** aktualisiert.<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                              | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die *x-, y-* und *z-Komponenten* eines normalen Vektors darstellen. Interne [**glNormal-Befehle**](glnormal-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuelle Normalität wird jedoch nicht mit dem Wert dieser **glNormal-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ \_ TEXTURKOORD \_ 1**</dt> </dl> | Jeder Kontrollpunkt ist ein einzelner Gleitkommawert, der die *Texturkoordinate* darstellt. Interne [**glTexCoord1-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ \_ TEXTURKOORD \_ 2**</dt> </dl> | Jeder Kontrollpunkt besteht aus zwei Gleitkommawerten, die die *Texturkoordinaten s* und *t* darstellen. Interne [**glTexCoord2-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ \_ TEXTURKOORD \_ 3**</dt> </dl> | Jeder Kontrollpunkt besteht aus drei Gleitkommawerten, die die *Texturkoordinaten s, t* und *r* darstellen. Interne [**glTexCoord3-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ \_ TEXTURKOORD \_ 4**</dt> </dl> | Jeder Kontrollpunkt besteht aus vier Gleitkommawerten, die die *Texturkoordinaten s, t, r* *und q* darstellen. Interne [**glTexCoord4-Befehle**](gltexcoord-functions.md) werden generiert, wenn die Zuordnung ausgewertet wird. Die aktuellen Texturkoordinaten werden jedoch nicht mit dem Wert dieser **glTexCoord-Befehle** aktualisiert.<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**glEvalCoord1**](glevalcoord-functions.md)dargestellt, zu *u*^, der Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*u2* 
</dt> <dd>

Eine lineare Zuordnung von *u*, wie [**glEvalCoord1**](glevalcoord-functions.md)dargestellt, zu *u*^, der Variablen, die von den durch diesen Befehl angegebenen Gleichungen ausgewertet wird.

</dd> <dt>

*Schritt* 
</dt> <dd>

Die Anzahl der Gleitkommazahlen oder Doubles zwischen dem Anfang eines Kontrollpunkts und dem Anfang des nächsten In der Datenstruktur, auf die in Punkt verwiesen *wird.* Dadurch können Steuerungspunkte in beliebige Datenstrukturen eingebettet werden. Die einzige Einschränkung ist, dass die Werte für einen bestimmten Kontrollpunkt zusammenhängende Speicherorte belegen müssen.

</dd> <dt>

*order* 
</dt> <dd>

Die Anzahl der Kontrollpunkte. Muss positiv sein.

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
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *u1* war gleich *u2.*<br/>                                                                                                    |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *stride* war kleiner als die Anzahl der Werte in einem Kontrollpunkt.<br/>                                                            |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *order* war kleiner als 1 oder GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                                         |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Auswertungen bieten eine Möglichkeit, polynomiale oder rationale polynomiale Zuordnung zu verwenden, um Scheitelungen, Normals, Texturkoordinaten und Farben zu erzeugen. Die von einer Auswertung erzeugten Werte werden an weitere Phasen der OpenGL-Verarbeitung gesendet, als ob sie mithilfe der Befehle [**glVertex,**](glvertex-functions.md) [**glNormal,**](glnormal-functions.md) [**glTexCoord**](gltexcoord-functions.md)und [**glColor**](glcolor-functions.md) dargestellt worden wäre, mit der Ausnahme, dass die generierten Werte nicht die aktuelle Normal- oder Texturkoordinate oder Farbe aktualisieren.

Alle polynomialen oder rationalen polynomialen Splines eines beliebigen Grads (bis zu dem von der OpenGL-Implementierung unterstützten maximalen Grad) können mithilfe von Auswertungen beschrieben werden. Dazu gehören fast alle Splines, die in Computergrafiken verwendet werden, einschließlich B-Splines, Bézierkurven, Hermite-Splines und so weiter.

Auswerter definieren Kurven basierend auf Polynomen von Polynomen. Definieren **Sie p** () als .

![Gleichung, die die Definition von p () zeigt.](images/map01.png)

wobei **R**_i_ ein Kontrollpunkt und () das *i* das Polynom "i" des *Grads n* (*Reihenfolge*  = *n* + 1) ist:

![Gleichung, die die Polynomie des Grads n zeigt.](images/map02.png)

Denken Sie daran, dass

![Gleichungen mit Äquivalenz zu 1.](images/map03.png)

Die **glMap1-Funktion** wird verwendet, um die Basis zu definieren und anzugeben, welche Art von Werten erzeugt werden. Nach der Definition kann eine Zuordnung aktiviert und deaktiviert werden, indem [**glEnable**](glenable.md) und **glDisable** mit dem Kartennamen, einem der neun vordefinierten Werte für das oben beschriebene Ziel, *aufruft.* Die [glEvalCoord1-Funktion](glevalcoord-functions.md) wertet die aktivierten eindimensionalen Karten aus. Wenn **glEvalCoord1 den** Wert *u* enthält, werden die Funktionen von "Funktionen" *mithilfe* von u ^ausgewertet, wobei

![Die Gleichung zeigt die Definition Von Ihnen^.](images/map04.png)

Die *Parameter stride,* *order* und *points* definieren die Array-Adressierung für den Zugriff auf die Kontrollpunkte. Der *Points-Parameter* ist die Position des ersten Kontrollpunkts, der je nachdem, welche Zuordnung definiert wird, einen, zwei, drei oder vier zusammenhängende Speicherorte einnimmt. Der *Order-Parameter* ist die Anzahl der Kontrollpunkte im Array. Der *stride-Parameter* gibt an, wie viele float- oder double-Positionen der interne Speicherzeiger so hoch schreitet, dass er den nächsten Kontrollpunkt erreicht.

Wie bei allen OpenGL-Befehlen, die Zeiger auf Daten akzeptieren,  wird der Inhalt von Punkten vor der Rückkehr von **glMap1** kopiert. Änderungen am Inhalt von *Punkten* haben nach dem Aufruf von **glMap1** keine Auswirkungen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glMap1** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ MAP1 \_ VERTEX \_ 3

**glIsEnabled** mit dem Argument GL \_ MAP1 \_ VERTEX \_ 4

**glIsEnabled** mit dem Argument GL \_ MAP1 \_ INDEX

**glIsEnabled** mit argument GL \_ MAP1 \_ COLOR \_ 4

**glIsEnabled** mit dem Argument GL \_ MAP1 \_ NORMAL

**glIsEnabled** mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled** mit dem Argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled** mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled** mit argument GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

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

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





