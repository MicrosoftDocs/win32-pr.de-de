---
title: glTexSubImage2D-Funktion (Gl.h)
description: Die glTexSubImage2D-Funktion gibt einen Teil eines vorhandenen eindimensionalen Texturbilds an. Sie können keine neue Textur mit glTexSubImage2D definieren.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c568afbe63ab01bd2866f180f968ea80101fec2ff22062707f4929d662ea47ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519700"
---
# <a name="gltexsubimage2d-function"></a>glTexSubImage2D-Funktion

Die **glTexSubImage2D-Funktion** gibt einen Teil eines vorhandenen eindimensionalen Texturbilds an. Sie können mit **glTexSubImage2D** keine neue Textur definieren.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur. Muss GL \_ TEXTURE \_ 2D sein.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer. Ebene 0 ist das Basisimage. Ebene *n* ist das Bild der *n-ten* Mipmapverringerung.

</dd> <dt>

*xoffset* 
</dt> <dd>

Ein Texeloffset  in x-Richtung innerhalb des Texturarrays.

</dd> <dt>

*yoffset* 
</dt> <dd>

Ein Texeloffset in *y-Richtung* innerhalb des Texturarrays.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturunterbilds.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Texturunterbilds.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Es kann einer der folgenden symbolischen Werte angenommen werden.



| Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Jedes Element ist ein einzelner Wert, ein Farbindex. Sie wird in ein Festkommaformat (mit einer nicht angegebenen Anzahl von 0 Bits rechts vom Binärpunkt) konvertiert, je nach Wert und Vorzeichen von GL INDEX SHIFT nach links oder rechts verschoben \_ und gl INDEX OFFSET hinzugefügt \_ \_ \_ (siehe [**glPixelTransfer**](glpixeltransfer.md)). Der resultierende Index wird mithilfe der Tabellen GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B und GL PIXEL MAP I TO A in einen Satz von Farbkomponenten konvertiert \_ \_ \_ und \_ \_ \_ \_ \_ \_ mit dem \_ \_ Bereich \_ \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1 \] verbunden.<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Jedes Element ist eine einzelne rote Komponente. Sie wird in das Gleitkommaformat konvertiert und in ein RGBA-Element zusammengesetzt, indem 0,0 für Grün und Blau und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Jedes Element ist eine einzelne grüne Komponente. Er wird in das Gleitkommaformat konvertiert und in ein RGBA-Element zusammengesetzt, indem 0,0 für Rot und Blau und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Jedes Element ist eine einzelne blaue Komponente. Sie wird in das Gleitkommaformat konvertiert und in ein RGBA-Element zusammengestellt, indem 0,0 für Rot und Grün und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Jedes Element ist eine einzelne Alphakomponente. Sie wird in das Gleitkommaformat konvertiert und zu einem RGBA-Element zusammengesetzt, indem 0,0 für Rot, Grün und Blau angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Jedes Element ist ein RGB-Triple. Sie wird in das Gleitkommaformat konvertiert und durch Anfügen von 1.0 für Alpha in ein RGBA-Element zusammengesetzt. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Jedes Element ist ein vollständiges RGBA-Element. Sie wird in Gleitkomma konvertiert. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Jedes Element ist ein einzelner Leuchtdichtewert. Er wird in das Gleitkommaformat konvertiert und dann zu einem RGBA-Element zusammengesetzt, indem der Leuchtwert dreimal für Rot, Grün und Blau repliziert und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Jedes Element ist ein Leuchtdichte-/Alphapaar. Sie wird in das Gleitkommaformat konvertiert und dann zu einem RGBA-Element zusammengesetzt, indem der Leuchtdichtewert dreimal für Rot, Grün und Blau repliziert wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der Pixeldaten. Die folgenden symbolischen Werte werden akzeptiert: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ \_ UNSIGNED \_ INT, GL \_ INT und GL \_ FLOAT.

</dd> <dt>

*Pixel* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Target* war nicht GL \_ TEXTURE \_ 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* war keine akzeptierte Konstante.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* war keine akzeptierte Konstante.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Type* war GL \_ BITMAP, und *das Format* war nicht GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder größer als log2 *max,* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ war.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *xoffset* war kleiner als -*b*; oder *xoffset*  +  *width* was greater than *w*  -  *b*; or *yoffset* was less than -*b*; or *yoffset*  +  *height* was greater than *h*  -  *b*, where *w* is the GL \_ TEXTURE \_ WIDTH, *h* is the GL \_ TEXTURE \_ HEIGHT, and *b* is the width of the GL TEXTURE BORDER of the texture image \_ being \_ modified. <br/> Beachten Sie, dass *w* und *h* die doppelte Rahmenbreite enthalten.<br/> |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als *b,* wobei *b* die Rahmenbreite des Texturarrays ist.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *border* war nicht null oder 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Das Texturarray wurde nicht durch einen vorherigen **glTexImage2D-Vorgang** definiert.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Hinweise

Die zweidimensionale Texturierung für einen Primitiven wird mit [**glEnable**](glenable.md) und **glDisable** mit dem Argument GL \_ TEXTURE \_ 2D aktiviert. Während der Texturierung wird ein Teil eines angegebenen Texturbilds jedem aktivierten Primitiven zugeordnet. Sie verwenden die **glTexSubImage2D-Funktion,** um ein zusammenhängendes Unterbild eines vorhandenen zweidimensionalen Texturbilds für die Textur anzugeben.

Die Texel,  auf die von Pixeln verwiesen wird, ersetzen einen Bereich des vorhandenen Texturarrays durch x-Indizes von *xoffset* und *xoffset* +*(* Breite 1) einschließlich und *y-Indizes* von *yoffset* und *yoffset* + (*height* 1) inclusive.  Dieser Bereich darf keine Texel außerhalb des Bereichs des ursprünglich angegebenen Texturarrays enthalten.

Das Angeben eines Unterbilds mit einer *Breite* von 0 (null) hat keine Auswirkungen und generiert keinen Fehler.

Die Texturierung hat keine Auswirkungen im Farbindexmodus.

Im Allgemeinen können Texturbilder durch dieselben Datenformate wie die Pixel in einem [**glDrawPixels-Befehl**](gldrawpixels.md) dargestellt werden, mit der Ausnahme, dass GL STENCIL INDEX und GL DEPTH COMPONENT nicht verwendet werden \_ \_ \_ \_ können. Die [**Modi glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich genau so auf Texturbilder aus, wie sie **glDrawPixels beeinflussen.**

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexSubImage2D ab:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ TEXTURE \_ 2D

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

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





