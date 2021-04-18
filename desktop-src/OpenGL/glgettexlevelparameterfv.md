---
title: glgettexlevelparameterfv-Funktion (GL. h)
description: Die Funktionen "glgettexlevelparameterfv" und "glgettexlevelparameteriv" geben Textur Parameterwerte für eine bestimmte Detailebene zurück. | glgettexlevelparameterfv-Funktion (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glgettexlevelparameterfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365037"
---
# <a name="glgettexlevelparameterfv-function"></a>glgettexlevelparameterfv-Funktion

Die Funktionen " **glgettexlevelparameterfv** " und " [**glgettexlevelparameteriv**](glgettexlevelparameteriv.md) " geben Textur Parameterwerte für eine bestimmte Detailebene zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Der symbolische Name der Ziel Textur: GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailstufe des gewünschten Bilds. Ebene 0 ist die Basis Image Ebene. Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name eines Textur Parameters. Die folgenden Parameternamen werden akzeptiert.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**GL- \_ Textur \_ Breite**</dt> </dl>                                | Der Parameter *para* meters gibt einen einzelnen Wert zurück, der die Breite des Textur Bilds enthält. Dieser Wert enthält den Rahmen des Textur Bilds.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**GL- \_ Textur \_ Höhe**</dt> </dl>                             | Der Parameter *para* meters gibt einen einzelnen Wert zurück, der die Höhe des Textur Bilds enthält. Dieser Wert enthält den Rahmen des Textur Bilds.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**Format der GL- \_ Textur \_ intern \_**</dt> </dl> | Der Parameter *para* meters gibt einen einzelnen Wert zurück, der das Texturformat der Textur beschreibt.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**GL- \_ Textur Rahmen \_**</dt> </dl>                             | Der Parameter *para* meters gibt einen einzelnen Wert zurück: die Breite des Rahmens des Textur Bilds in Pixel.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**\_Größe der \_ \_ Größen Größe von GL**</dt> </dl>                      | Die interne speicherauflösung der roten Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**GL- \_ Textur- \_ grün \_ Größe**</dt> </dl>                | Die interne speicherauflösung der grünen Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**GL- \_ Textur \_ blau- \_ Größe**</dt> </dl>                   | Die interne speicherauflösung der blauen Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**GL- \_ Textur \_ alpha \_ Größe**</dt> </dl>                | Die interne speicherauflösung der Alpha Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**GL- \_ Textur- \_ Beleuchtungs \_ Größe**</dt> </dl>    | Die interne speicherauflösung der Leuchtkraft Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**Größe der GL- \_ Textur \_ Intensität \_**</dt> </dl>    | Die interne speicherauflösung der Intensität-Komponente eines Texels. Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**GL- \_ Textur \_ Komponenten**</dt> </dl>                 | Der Parameter *para* meters gibt einen einzelnen Wert zurück: die Anzahl der Komponenten im Textur Bild.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *target* oder *PName* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* ist kleiner als 0 (null) oder größer als *Log* 2 *(max)*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ texture size ist \_ .<br/>      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgettexlevelparameter** " *gibt in* parameterparameterwerten für eine bestimmte Detailstufe, die als *Ebene* angegeben ist, zurück. Der *Ziel* Parameter definiert die Ziel Textur, entweder GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ Proxy \_ Textur \_ 1D oder GL \_ -Proxy \_ Textur \_ 2D, um eindimensionale oder zweidimensionale Texturierung anzugeben. Der *PName* -Parameter gibt den Texture-Parameter an, dessen Wert oder Werte zurückgegeben werden.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.

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

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





