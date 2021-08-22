---
title: glTexGend-Funktion (Gl.h)
description: Steuert die Generierung von Texturkoordinaten. | glTexGend-Funktion (Gl.h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- glTexGend-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b05d390c935047065febdb86e9d9c4c68758648b76641c346629c0cde4be5dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490444"
---
# <a name="gltexgend-function"></a>glTexGend-Funktion

Steuert die Generierung von Texturkoordinaten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Coord* 
</dt> <dd>

Eine Texturkoordinate. Dies muss einer der folgenden Sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

Der symbolische Name der Texturkoordinatengenerierungsfunktion.

</dd> <dt>

*param* 
</dt> <dd>

Ein einwertiger Texturgenerierungsparameter, einer von GL \_ OBJECT \_ LINEAR, GL \_ EYE LINEAR oder GL SPHERE \_ \_ \_ MAP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *coord* oder *pname* war kein akzeptierter definierter Wert, oder *pname* war GL TEXTURE GEN MODE, und \_ \_ \_ *params* waren kein akzeptierter definierter Wert.<br/> |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname war* GL \_ TEXTURE GEN \_ \_ MODE, *params* war GL SPHERE MAP, und \_ \_ *coord* war \_ \_ entweder GL R oder GL Q<br/>                                     |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md) <br/>                 |



## <a name="remarks"></a>Hinweise

Die **glTexGen-Funktion** wählt eine Texturkoordinatengenerierungsfunktion aus oder stellt Koeffizienten für eine der Funktionen zur Verfügung. Der *koord-Parameter* benennt eine der Texturkoordinaten (s,t,r,q), und es muss eines der folgenden Symbole sein: GL \_ S, GL T, GL R oder GL \_ \_ \_ Q. Der *pname-Parameter* muss eine von drei symbolischen Konstanten sein: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE oder GL \_ EYE \_ \_ \_ PLANE. Wenn *pname GL* TEXTURE GEN MODE ist, gibt param einen Modus an, einen von \_ GL OBJECT \_ \_  \_ \_ LINEAR, GL EYE LINEAR \_ oder GL SPHERE \_ \_ \_ MAP. Wenn *pname entweder* GL OBJECT PLANE oder GL EYE PLANE ist, enthält \_ \_ \_ \_ *param* Koeffizienten für die entsprechende Texturgenerierungsfunktion.

Wenn die Texturgenerierungsfunktion GL \_ OBJECT \_ LINEAR ist, die Funktion

![Gleichung, die die glTexGen-Funktion zeigt, wenn die Texturgenerierungsfunktion GL_OBJECT_LINEAR.](images/tex02.png)

wird verwendet, wobei g der Wert ist, der für die koord benannte Koordinate berechnet wird. p1, p2, p3 und p4 sind die vier Werte, die in Parametern angegeben werden. und x?, y?, z? und w? sind die Objektkoordinaten des Scheitelpunkts. Sie können diese Funktion zum Strukturieren von Gelände verwenden, indem Sie den Seepegel als Referenzebene verwenden (definiert durch p1, p2, p3 und p4). Die GL OBJECT LINEAR-Koordinatengenerierungsfunktion berechnet die Höhe eines Geländevertex als Entfernung vom Seeniveau. Diese Höhe wird verwendet, um das Texturbild zu indizieren, um z. B. Weißen Schnee auf Spitzen und grünes Grünland auf Fußflächen zu \_ \_ ordnen.

Wenn die Texturgenerierungsfunktion GL \_ EYE \_ LINEAR ist, die Funktion

![Gleichung, die die glTexGen-Funktion zeigt, wenn die Texturgenerierungsfunktion GL_EYE_LINEAR.](images/tex02.png)

wird verwendet, wobei

![Gleichung, die die Augenkoordinaten des Scheitelpunkts zeigt.](images/tex03.png)

und x?, y?, z? und w? sind die Augenkoordinaten des Scheitelpunkts, p1, p2, p3 und p4 sind die Werte, die im *Parameter* angegeben werden, und M ist die Modellansichtsmatrix, wenn Sie **glTexGen aufrufen.** Wenn M schlecht konditioniert oder singulär ist, können texturkoordinaten, die von der resultierenden Funktion generiert werden, ungenau oder nicht definiert sein.

Die Werte im *Parameter definieren* eine Verweisebene in Augenkoordinaten. Die modelview-Matrix, die auf sie angewendet wird, darf nicht dieselbe sein, wenn die Polygonvertices transformiert werden. Diese Funktion richtet ein Feld von Texturkoordinaten ein, die dynamische Konturlinien für sich bewegende Objekte erzeugen können.

Wenn *pname* GL \_ SPHERE MAP und \_ *coord* entweder GL S oder GL T ist, werden die Texturkoordinaten s und \_ t wie folgt \_ generiert. Lassen Sie uns den Einheitenvektor verwenden, der vom Ursprung auf den Polygonvertex (in Augenkoordinaten) zeigen soll. Lassen Sie uns nach der Transformation in Augenkoordinaten die aktuelle Normalität sein. Lassen Sie f = (fx ( ) fy ( ) fz)T der Reflektionsvektor sein, damit

![Gleichung, die den Reflektionsvektor als Funktion des Einheitenvektors und der aktuellen Normalität zeigt.](images/tex05.png)

Lassen Sie abschließend

![Gleichung, die m als Funktion des Reflektionsvektors zeigt.](images/tex07.png)

Dann sind die Werte, die den Texturkoordinaten i und t zugewiesen sind,

![Die Gleichung zeigt werte, die den Texturkoordinaten i und t zugewiesen sind.](images/tex06.png)

Sie können eine Texturkoordinatengenerierungsfunktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**glDisable**](gldisable.md) mit einem der symbolischen Texturkoordinatennamen (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN T, GL TEXTURE GEN R oder GL TEXTURE GEN Q) als Argument \_ \_ \_ \_ \_ \_ \_ \_ \_ verwenden. Wenn diese Funktion aktiviert ist, wird die angegebene Texturkoordinate gemäß der generierenden Funktion berechnet, die dieser Koordinate zugeordnet ist. Wenn die Funktion deaktiviert ist, übernehmen nachfolgende Scheitelungen die angegebene Texturkoordinate aus dem aktuellen Satz von Texturkoordinaten. Anfänglich sind alle Texturgenerierungsfunktionen auf GL \_ EYE LINEAR festgelegt und \_ deaktiviert. Beide Gleichungen der Ebene sind (1,0,0,0); Beide Gleichungen der T-Ebene sind (0,1,0,0); und alle r- und q-Ebenengleichungen sind (0,0,0,0).

Die folgenden Funktionen rufen Informationen im Zusammenhang mit glTexGen ab:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled mit Argument**](glisenabled.md) GL \_ TEXTURE GEN \_ \_ S  
[**glIsEnabled mit Argument**](glisenabled.md) GL \_ TEXTURE GEN \_ \_ T  
[**glIsEnabled mit Argument**](glisenabled.md) GL \_ TEXTURE GEN \_ \_ R  
[**glIsEnabled mit Argument**](glisenabled.md) GL \_ TEXTURE GEN \_ \_ Q  
</dl>

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

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





