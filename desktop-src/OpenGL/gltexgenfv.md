---
title: gltexgenfv-Funktion (GL. h)
description: Steuert die Generierung von Texturkoordinaten. | gltexgenfv-Funktion (GL. h)
ms.assetid: d5454d6f-16bb-47d9-9c52-da2daf491224
keywords:
- gltexgenfv-Funktion OpenGL
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
ms.openlocfilehash: f4d5394b6385246f296a472ce51f2727e2738845
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104550979"
---
# <a name="gltexgenfv-function"></a>gltexgenfv-Funktion

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

*Koord* 
</dt> <dd>

Eine Textur Koordinate. Muss eines der folgenden sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.

</dd> <dt>

**pName** 
</dt> <dd>

Der symbolische Name der Texturkoordinaten Generierungs Funktion.

</dd> <dt>

*params* 
</dt> <dd>

Ein Array von Gleit Komma Zahlen, das die Koeffizienten für die entsprechende Textur Generierungs Funktion enthält.

``` syntax
GLfloat zPlane[] = { 0.0f, 0.0f, 1.0f, 0.0f };
```

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *coord* oder *PName* war kein akzeptierter definierter Wert, oder *PName* war der \_ GL \_ -Textur gen \_ -Modus, und der Parameter war kein akzeptierter definierter Wert. <br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/>                 |



## <a name="remarks"></a>Bemerkungen

Die **gltexgen** -Funktion wählt eine Texturkoordinaten-Generierungs Funktion aus oder liefert Koeffizienten für eine der Funktionen. Der *coord* -Parameter benennt eine der (s, t, r, q)-Texturkoordinaten und muss eines der folgenden Symbole sein: GL \_ s, GL \_ t, GL \_ r oder GL \_ q. Der *PName* -Parameter muss eine von drei symbolischen Konstanten sein: GL \_ Texture \_ gen- \_ Modus, GL- \_ Objekt \_ Ebene oder GL- \_ Eye- \_ Ebene. Wenn *PName* entweder eine GL- \_ Objekt \_ Ebene oder \_ eine GL-Augen Ebene ist \_ , enthält *param* Koeffizienten für die entsprechende Textur Generierungs Funktion.

Wenn die Textur Generierungs Funktion ein GL- \_ Objekt \_ linear ist, wird die Funktion

! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_OBJECT_LINEAR ist.]

wird verwendet, wobei g der Wert ist, der für die in coord benannte Koordinate berechnet wird. P1, P2, P3 und P4 sind die vier Werte, die in Parametern bereitgestellt werden. und x?, y?, z? und w? die Objekt Koordinaten des Scheitel Punkts. Sie können diese Funktion verwenden, um das Gelände mithilfe der Meeres Ebene als Bezugs Ebene (definiert durch P1, P2, P3 und P4) zu strukturieren. Die Funktion für die \_ \_ lineare Koordinaten Generierung von GL-Objekten berechnet die Höhe eines Gelände Scheitel Punkts als Abstand von der Meeres Ebene. diese Höhe wird zum Indizieren des Textur Bilds verwendet, um die Spitzen und das grüne Gras zum Rand zu ordnen.

Wenn die Textur Generierungs Funktion "GL \_ Eye linear" ist \_ , wird die Funktion

! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_EYE_LINEAR ist.]

wird verwendet, wobei

![Gleichung, die die Augen Koordinaten des Scheitel Punkts anzeigt.](images/tex03.png)

und x?, y?, z? und w? die Augen Koordinaten des Scheitel Punkts, P1, P2, P3 und P4 sind die Werte, die in *param* angegeben werden, und M ist die Modelview-Matrix, wenn Sie **gltexgen** aufrufen. Wenn M unzureichend bedingt oder Singular ist, können die von der resultierenden Funktion generierten Texturkoordinaten ungenau oder undefiniert sein.

Beachten Sie, dass die Werte in *param* eine Verweis Ebene in den Augen Koordinaten definieren. Die Modelview-Matrix, die auf Sie angewendet wird, ist möglicherweise nicht identisch, wenn die Polygon Scheitel Punkte transformiert werden. Diese Funktion legt ein Feld von Texturkoordinaten fest, das dynamische Konturlinien für das Verschieben von Objekten erzeugt.

Wenn " *PName* " den Wert "GL \_ Sphere \_ map" und " *coord* " entweder "GL \_ s" oder "GL t" ist \_ , werden die S-und T-Texturkoordinaten U. a. der Einheits Vektor, der vom Ursprung auf den Polygon Scheitelpunkt zeigt (in Augen Koordinaten). Let n ist die aktuelle normale, nach der Transformation zu den Augen Koordinaten. Let f = (FX () fy () FZ) T der reflektionvektor, damit

![Gleichung, die den Reflektionsvektor als Funktion des Einheits Vektors und des aktuellen normalen anzeigt.](images/tex05.png)

Und schließlich

![Gleichung, die m als Funktion des reflektionsvektors anzeigt.](images/tex07.png)

Dann sind die den i-und t-Texturkoordinaten zugewiesenen Werte

![Gleichung, die den i-und t-Texturkoordinaten zugewiesene Werte anzeigt.](images/tex06.png)

Sie können eine Texturkoordinaten-Generierungs Funktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**gldeaktivieren**](gldisable.md) mit einem der symbolischen Texturkoordinaten Namen (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R oder GL \_ Texture \_ gen \_ Q) als Argument verwenden. Wenn diese Funktion aktiviert ist, wird die angegebene Textur Koordinate entsprechend der der Koordinate zugeordneten Generierungs Funktion berechnet. Wenn diese Funktion deaktiviert ist, nehmen nachfolgende Vertices die angegebene Textur Koordinate aus dem aktuellen Satz von Texturkoordinaten an. Anfänglich werden alle Textur Generierungs Funktionen auf "GL Eye linear" festgelegt \_ \_ und sind deaktiviert. Beide s-Ebenen-Gleichungen sind (1, 0, 0, 0); Beide t-Ebenen-Gleichungen sind (0, 1, 0, 0); und alle Gleichungen der r-und q-Ebene sind (0, 0, 0, 0).

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit gltexgen abgerufen:

<dl>

[**glgettexgen**](glgettexgen.md)  
[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ S  
[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ T  
[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ R  
[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ Q  
</dl>

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

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glgettexgen**](glgettexgen.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[gltexd](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[gltexparameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





