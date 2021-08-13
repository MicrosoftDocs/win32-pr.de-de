---
title: glTexGenfv-Funktion (Gl.h)
description: Steuert die Generierung von Texturkoordinaten. | glTexGenfv-Funktion (Gl.h)
ms.assetid: d5454d6f-16bb-47d9-9c52-da2daf491224
keywords:
- glTexGenfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexGenfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e7e7760eacc22f7ea47fa2e6fa2d9d9dab02d1499236dd02985d6f818d54f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613325"
---
# <a name="gltexgenfv-function"></a>glTexGenfv-Funktion

Steuert die Generierung von Texturkoordinaten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexGenfv(
         GLenum  coord,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Coord* 
</dt> <dd>

Eine Texturkoordinate. Muss einer der folgenden Sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

Der symbolische Name der Texturkoordinatengenerierungsfunktion.

</dd> <dt>

*params* 
</dt> <dd>

Ein Array von Gleitkommawerten, das die Koeffizienten für die entsprechende Texturgenerierungsfunktion enthält.

``` syntax
GLfloat zPlane[] = { 0.0f, 0.0f, 1.0f, 0.0f };
```

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *coord* oder *pname* war kein akzeptierter definierter Wert, oder *pname* war GL \_ TEXTURE GEN MODE und \_ \_ *params* war kein akzeptierter definierter Wert.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/>                 |



## <a name="remarks"></a>Hinweise

Die **glTexGen-Funktion** wählt eine Texturkoordinatengenerierungsfunktion aus oder stellt Koeffizienten für eine der Funktionen zur Verfügung. Der *Coord-Parameter* benennt eine der Texturkoordinaten (s,t,r,q) und muss eines dieser Symbole sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q. Der *pname-Parameter* muss eine von drei symbolischen Konstanten sein: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE oder GL \_ EYE \_ \_ \_ PLANE. Wenn *pname* entweder GL \_ OBJECT PLANE oder GL EYE PLANE \_ \_ \_ ist, enthält *param* Koeffizienten für die entsprechende Texturgenerierungsfunktion.

Wenn die Texturgenerierungsfunktion GL \_ OBJECT \_ LINEAR ist, die Funktion

! [Gleichung, die die glTexGen-Funktion zeigt, wenn die Texturgenerierungsfunktion GL_OBJECT_LINEAR ist.]

wird verwendet, wobei g der Wert ist, der für die Koordinate mit dem Namen in coord berechnet wird. p1, p2, p3 und p4 sind die vier Werte, die in Parametern bereitgestellt werden. und x?, y?, z? und w? sind die Objektkoordinaten des Scheitelpunkts. Sie können diese Funktion verwenden, um ein Gelände zu strukturieren, indem Sie den Seegrad als Referenzebene verwenden (definiert durch p1, p2, p3 und p4). Die \_ GL OBJECT \_ LINEAR-Koordinategenerierungsfunktion berechnet die Höhe eines Geländevertex als Abstand zum Wasserstand. Diese Höhe wird verwendet, um das Texturbild zu indizieren, um weißer Schnee auf Spitzen und grünem Rasen z. B. Fußnoten zuzuordnen.

Wenn die Texturgenerierungsfunktion GL \_ EYE \_ LINEAR ist, die Funktion

! [Gleichung, die die glTexGen-Funktion zeigt, wenn die Texturgenerierungsfunktion GL_EYE_LINEAR ist.]

wird verwendet, wobei

![Gleichung, die die Augenkoordinaten des Scheitelpunkts anzeigt.](images/tex03.png)

und x?, y?, z? und w? sind die Augenkoordinaten des Scheitelpunkts, p1, p2, p3 und p4 sind die werte, die im *Parameter* angegeben sind, und M ist die Modellansichtsmatrix, wenn Sie **glTexGen** aufrufen. Wenn M schlecht konditioniert oder singular ist, können texturkoordinaten, die von der resultierenden Funktion generiert werden, ungenau oder nicht definiert sein.

Beachten Sie, dass die Werte in *param* eine Verweisebene in Augenkoordinaten definieren. Die Modellansichtsmatrix, die auf sie angewendet wird, ist möglicherweise nicht identisch, wenn die Polygonvertices transformiert werden. Diese Funktion richtet ein Feld von Texturkoordinaten ein, das dynamische Konturlinien für sich bewegende Objekte erzeugen kann.

Wenn *pname* GL \_ SPHERE MAP und \_ *coord* entweder GL \_ S oder GL T \_ ist, werden die Texturkoordinaten s und t wie folgt generiert. Lassen Sie uns der Einheitenvektor sein, der vom Ursprung auf den Polygonvertex (in Augenkoordinaten) verweist. Lassen Sie n die aktuelle Normalität nach der Transformation zu Augenkoordinaten sein. Lassen Sie f = (fx ( ) fy ( ) fz)T der Reflektionsvektor sein, sodass

![Gleichung, die den Reflektionsvektor als Funktion des Einheitenvektors und der aktuellen Normalität zeigt.](images/tex05.png)

Lassen Sie uns abschließend

![Gleichung, die m als Funktion des Reflektionsvektors zeigt.](images/tex07.png)

Dann sind die Werte, die den i- und t-Texturkoordinaten zugewiesen sind,

![Gleichung mit Werten, die den i- und t-Texturkoordinaten zugewiesen sind.](images/tex06.png)

Sie können eine Texturkoordinatengenerierungsfunktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**glDisable**](gldisable.md) mit einem der symbolischen Texturkoordinatennamen (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN \_ \_ \_ T, GL TEXTURE GEN R \_ oder GL TEXTURE GEN \_ \_ \_ \_ \_ Q) als Argument verwenden. Wenn diese Funktion aktiviert ist, wird die angegebene Texturkoordinate entsprechend der generierenden Funktion berechnet, die dieser Koordinate zugeordnet ist. Wenn diese Funktion deaktiviert ist, übernehmen nachfolgende Scheitelpunkte die angegebene Texturkoordinate aus dem aktuellen Satz von Texturkoordinaten. Anfänglich werden alle Funktionen zur Texturgenerierung auf GL EYE LINEAR festgelegt \_ \_ und deaktiviert. Beide Ebenengleichungen sind (1,0,0,0); beide t-Ebenengleichungen sind (0,1,0,0); und alle Formeln der R- und Q-Ebene sind (0,0,0,0).

Die folgenden Funktionen rufen Informationen im Zusammenhang mit glTexGen ab:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ GEN \_ S  
[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ GEN \_ T  
[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ GEN \_ R  
[**glIsEnabled**](glisenabled.md) mit argument GL \_ TEXTURE \_ GEN \_ Q  
</dl>

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

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[glTexParameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





