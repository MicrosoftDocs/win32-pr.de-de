---
title: glTexImage1D-Funktion (Gl.h)
description: Die glTexImage1D-Funktion gibt ein eindimensionales Texturbild an.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd443389439b6d012533d3184739dfa849d672d76a8eced0e8ea244601d4122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490250"
---
# <a name="glteximage1d-function"></a>glTexImage1D-Funktion

Die **glTexImage1D-Funktion** gibt ein eindimensionales Texturbild an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur. Muss GL \_ TEXTURE \_ 1D sein.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebenennummer. Ebene 0 ist die Basisimageebene. Ebene *n* ist das nTh-Mipmap-Reduzierungsbild. 

</dd> <dt>

*internalformat* 
</dt> <dd>

Gibt die Anzahl der Farbkomponenten in der Textur an. Muss 1, 2, 3 oder 4 oder eine der folgenden symbolischen Konstanten sein: GL \_ ALPHA, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ LUMINANCE, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ LUMINANCE \_ ALPHA, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ LUMINANCE, GL LUMINANCE, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ RGB, GL \_ R3 \_ G3 \_ B2, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ A1, GL \_ RGBA8, GL \_ RGB10 \_ A2, GL \_ RGBA12 oder GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Texturbilds. Muss 2 *n* + 2( *Border* ) für eine ganze Zahl *n sein.* Die Höhe des Texturbilds ist 1.

</dd> <dt>

*Grenze* 
</dt> <dd>

Die Breite des Rahmens. Muss entweder 0 oder 1 sein.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Es kann einer von neun symbolischen Werten angenommen werden.



| Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Jedes Element ist ein einzelner Wert, ein Farbindex. Er wird in einen festen Punkt konvertiert (mit einer nicht angegebenen Anzahl von 0 Bits rechts vom Binärpunkt), nach links oder rechts verschoben, je nach Wert und Vorzeichen von GL \_ INDEX \_ SHIFT, und zu GL INDEX OFFSET hinzugefügt \_ \_ (siehe [**glPixelTransfer**](glpixeltransfer.md)). Der resultierende Index wird mithilfe der Tabellen GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B und GL PIXEL MAP I TO A in einen Satz von Farbkomponenten konvertiert \_ \_ \_ und \_ \_ \_ \_ \_ \_ mit dem \_ \_ Bereich \_ \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1 \] verbunden.<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Jedes Element ist eine einzelne rote Komponente. Sie wird in Gleitkomma konvertiert und in ein RGBA-Element zusammengesetzt, indem 0,0 für Grün und Blau und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Jedes Element ist eine einzelne grüne Komponente. Sie wird in Gleitkomma konvertiert und zu einem RGBA-Element zusammengesetzt, indem 0,0 für Rot und Blau und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Jedes Element ist eine einzelne blaue Komponente. Sie wird in Gleitkomma konvertiert und in ein RGBA-Element zusammengesetzt, indem 0,0 für Rot und Grün und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Jedes Element ist eine einzelne rote Komponente. Sie wird in Gleitkomma konvertiert und zu einem RGBA-Element zusammengesetzt, indem 0,0 für Rot, Grün und Blau angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Jedes Element ist ein RGB-Triple. Sie wird in Gleitkomma konvertiert und durch Anfügen von 1.0 für Alpha in ein RGBA-Element zusammengesetzt. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Jedes Element ist ein vollständiges RGBA-Element. Sie wird in Gleitkomma konvertiert. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ EXT**</dt> </dl>                         | Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL \_ BGR \_ EXT bietet ein Format, das dem Speicherlayout von Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ EXT**</dt> </dl>                      | Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br/> GL \_ BGRA \_ EXT bietet ein Format, das dem Speicherlayout von Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Jedes Element ist ein einzelner Leuchtdichtewert. Er wird in Gleitkomma konvertiert und dann zu einem RGBA-Element zusammengesetzt, indem der Leuchtdichtewert dreimal für Rot, Grün und Blau repliziert und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Jedes Element ist ein Leuchtdichte-/Alphapaar. Sie wird in Gleitkomma konvertiert und dann zu einem RGBA-Element zusammengefügt, indem der Leuchtwert dreimal für Rot, Grün und Blau repliziert wird. Jede Komponente wird dann mit dem signierten Skalierungsfaktor GL \_ c \_ SCALE multipliziert, dem signierten Bias GL c BIAS hinzugefügt \_ und an den Bereich \_ \[ 0,1 gebunden \] (siehe **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* war keine GL \_ TEXTURE.<br/>                                                                                                                                                                                    |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* war keine akzeptierte Formatkonstante.  Es werden nur andere Formatkonstanten als GL \_ STENCIL \_ INDEX und GL DEPTH COMPONENT \_ \_ akzeptiert. Eine Liste möglicher Werte finden Sie in der Parameterbeschreibung des *Formats.*<br/> |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* war keine Typkonstante. <br/>                                                                                                                                                                                   |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Type* war GL \_ BITMAP, und *das Format* war nicht GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                        |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *level* war kleiner als 0 (null) oder größer als log2 *max,* wobei *max* der zurückgegebene Wert von GL \_ MAX TEXTURE SIZE \_ \_ war.<br/>                                                                                                 |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *internalformat* war nicht 1, 2, 3 oder 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als 0 (null) oder größer als 2 + GL \_ MAX TEXTURE \_ \_ SIZE, oder sie konnte nicht als 2 *n* + 2 (Rahmen) für einen ganzzahligen Wert von *n* dargestellt werden.<br/>                                                            |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *border* war nicht 0 oder 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>                                                                                          |



## <a name="remarks"></a>Hinweise

Die **glTexImage1D-Funktion** gibt ein eindimensionales Texturbild an. Die Texturierung ordnet einen Teil eines angegebenen *Texturbilds* jedem grafischen Primitiven zu, für das Texturierung aktiviert ist. Die eindimensionale Texturierung wird mit [**glEnable**](glenable.md) und **glDisable** mit dem Argument GL \_ TEXTURE \_ 1D aktiviert und deaktiviert.

Texturbilder werden mit **glTexImage1D definiert.** Die Argumente beschreiben die Parameter des Texturbilds, z. B. Breite, Breite des Rahmens, Detailebenennummer (siehe [**glTexParameter**](gltexparameter-functions.md)) und Anzahl der bereitgestellten Farbkomponenten. Die letzten drei Argumente beschreiben die Darstellung des Bilds im Arbeitsspeicher. Diese Argumente sind identisch mit den Pixelformaten, die für [**glDrawPixels verwendet werden.**](gldrawpixels.md)

Daten werden aus *Pixeln* als Sequenz von Bytes mit oder ohne Vorzeichen, Shorts oder Longs oder Gleitkommawerten mit einzelner Genauigkeit gelesen, je nach *Typ*. Diese Werte werden je nach Format in Sätze von einem, zwei, drei oder vier Werten zum Bilden von Elementen gruppiert. Wenn *type* GL BITMAP ist, werden die Daten als Zeichenfolge von Bytes ohne Vorzeichen betrachtet \_ (und das *Format* muss GL COLOR \_ INDEX \_ sein). Jedes Daten byte wird als acht 1-Bit-Elemente behandelt, und die Bit reihenfolge wird durch GL \_ UNPACK \_ LSB \_ FIRST bestimmt (siehe [**glPixelStore**](glpixelstore-functions.md)).

Ein Texturbild kann je nach Komponenten bis zu vier Komponenten pro Texturelement *aufweisen.* Ein Texturbild mit einer Komponente verwendet nur die rote Komponente der RGBA-Farbe, die aus Pixeln *extrahiert wurde.* Ein Bild mit zwei Komponenten verwendet die R- und A-Werte. Ein Image mit drei Komponenten verwendet die R-, G- und B-Werte. Ein Bild mit vier Komponenten verwendet alle RGBA-Komponenten.

Die Texturierung hat keine Auswirkungen im Farbindexmodus.

Das Texturbild kann durch die gleichen Datenformate wie die Pixel in einem [**glDrawPixels-Befehl**](gldrawpixels.md) dargestellt werden, mit der Ausnahme, dass GL STENCIL INDEX und GL DEPTH COMPONENT nicht \_ verwendet werden \_ \_ \_ können. Die [**Modi glPixelStore**](glpixelstore-functions.md) und [**glPixelTransfer**](glpixeltransfer.md) wirken sich genau so auf Texturbilder aus, wie sie **glDrawPixels beeinflussen.**

Ein Texturbild mit einer Breite von 0 (null) gibt die NULL-Textur an. Wenn die NULL-Textur für Detailebene 0 angegeben wird, ist dies so, als wäre die Texturierung deaktiviert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexImageID ab:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ TEXTURE \_ 1D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

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

[**glEnd**](glend.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





