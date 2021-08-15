---
title: glGetTexLevelParameterfv-Funktion (Gl.h)
description: Die Funktionen glGetTexLevelParameterfv und glGetTexLevelParameteriv geben Texturparameterwerte für eine bestimmte Detailebene zurück. | glGetTexLevelParameterfv-Funktion (Gl.h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glGetTexLevelParameterfv-Funktion OpenGL
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
ms.openlocfilehash: 1b4068b6544c334c4ca1c8e6640ccb4752669240cdde16d0522a4e13d06ebc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359776"
---
# <a name="glgettexlevelparameterfv-function"></a>glGetTexLevelParameterfv-Funktion

Die **Funktionen glGetTexLevelParameterfv** und [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) geben Texturparameterwerte für eine bestimmte Detailebene zurück.

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

Der symbolische Name der Zieltextur: GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE \_ \_ 1D oder GL \_ PROXY TEXTURE \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer des gewünschten Bilds. Ebene 0 ist die Basisimageebene. Ebene *n* ist das *n-te* Mipmap-Reduzierungsbild.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name eines Texturparameters. Die folgenden Parameternamen werden akzeptiert.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**GL \_ \_ TEXTURBREITE**</dt> </dl>                                | Der *Parameter params* gibt einen einzelnen Wert zurück, der die Breite des Texturbilds enthält. Dieser Wert schließt den Rahmen des Texturbilds ein.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**GL \_ \_ TEXTURHÖHE**</dt> </dl>                             | Der *Parameter params* gibt einen einzelnen Wert zurück, der die Höhe des Texturbilds enthält. Dieser Wert schließt den Rahmen des Texturbilds ein.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**INTERNES \_ \_ \_ GL-TEXTURFORMAT**</dt> </dl> | Der *Parameter params* gibt einen einzelnen Wert zurück, der das Texelformat der Textur beschreibt.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**GL \_ TEXTURE \_ BORDER**</dt> </dl>                             | Der *Parameter params* gibt einen einzelnen Wert zurück: die Breite des Rahmens des Texturbilds in Pixel.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**GL \_ TEXTURE \_ RED \_ SIZE**</dt> </dl>                      | Die interne Speicherauflösung der roten Komponente eines Texels. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**GL \_ TEXTURE \_ GREEN \_ SIZE**</dt> </dl>                | Die interne Speicherauflösung der grünen Komponente eines Texel. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**GL \_ \_ \_ TEXTURBLAUE GRÖßE**</dt> </dl>                   | Die interne Speicherauflösung der blauen Komponente eines Texels. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**GL \_ TEXTURE \_ ALPHA \_ SIZE**</dt> </dl>                | Die interne Speicherauflösung der Alphakomponente eines Texels. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**GL \_ TEXTUR \_ LUDOMINANZGRÖßE \_**</dt> </dl>    | Die interne Speicherauflösung der Leuchtdichtekomponente eines Texels. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**GL \_ TEXTURE \_ INTENSITY \_ SIZE**</dt> </dl>    | Die interne Speicherauflösung der Intensitätskomponente eines Texels. Die von OpenGL gewählte Auflösung ist eine enge Übereinstimmung mit der vom Benutzer angeforderten Auflösung mit dem Komponentenargument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**\_ \_ GL-TEXTURKOMPONENTEN**</dt> </dl>                 | Der *Parameter params* gibt einen einzelnen Wert zurück: die Anzahl der Komponenten im Texturbild.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *pname* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* ist kleiner als 0 (null) oder größer als *Protokoll* 2 *(max)*, wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ ist.<br/>      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetTexLevelParameter-Funktion** gibt in Parametertexturparameterwerten für einen bestimmten Detailebenenwert zurück, der als Ebene *angegeben ist.*  Der *Zielparameter* definiert die Zieltextur, entweder GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE \_ \_ 1D oder GL \_ PROXY TEXTURE \_ \_ 2D, um eindimensionale oder zweidimensionale Textur anzugeben. Der *pname-Parameter* gibt den Texturparameter an, dessen Wert oder Werte zurückgegeben werden.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt der *Parameter vorgenommen.*

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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





