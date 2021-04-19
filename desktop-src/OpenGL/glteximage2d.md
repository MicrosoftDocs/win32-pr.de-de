---
title: glTexImage2D-Funktion (GL. h)
description: Die glTexImage2D-Funktion gibt ein zweidimensionales Textur Bild an.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346771"
---
# <a name="glteximage2d-function"></a>glTexImage2D-Funktion

Die **glTexImage2D** -Funktion gibt ein zweidimensionales Textur Bild an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
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

Die Ziel Textur. Muss "GL \_ Texture \_ 2D" lauten.

</dd> <dt>

*level* 
</dt> <dd>

Die Detailebene. Ebene 0 ist die Basis Image Ebene. Ebene *n* ist das *n* -te MipMap-Reduzierungs Bild.

</dd> <dt>

*internalformat* 
</dt> <dd>

Die Anzahl der Farbkomponenten in der Textur. Muss 1, 2, 3 oder 4 sein oder eine der folgenden symbolischen Konstanten sein: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ Luminance, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensität, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ a1, GL \_ RGBA8, GL \_ RGB10 \_ a2, GL \_ RGBA12 oder GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Textur Bilds. Muss für eine Ganzzahl *n* 2 *n* +*2 (Rahmen*) lauten.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Textur Bilds. Muss für ein ganzzahliges *m* 2 *<sup>m</sup>* +*2 (Rahmen*) sein.

</dd> <dt>

*Aun* 
</dt> <dd>

Die Breite des Rahmens. Muss entweder 0 oder 1 sein.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Es kann einen von neun symbolischen Werten annehmen.



| Wert                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL- \_ Farb \_ Index**</dt> </dl>             | Jedes Element ist ein einzelner Wert, ein Farbindex. Es wird in einen festgelegten Punkt (mit einer nicht angegebenen Anzahl von 0 Bits rechts neben dem binären Punkt) konvertiert, abhängig vom Wert und Vorzeichen der GL-Index Verschiebung nach links oder rechts verschoben \_ \_ und dem GL- \_ Index \_ Offset (siehe [**glpixeltransfer**](glpixeltransfer.md)) hinzugefügt. Der resultierende Index wird mithilfe von GL \_ Pixel \_ map \_ i to \_ \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B und GL Pixel Map i to a Tables in eine Gruppe von Farbkomponenten konvertiert \_ \_ \_ \_ \_ und an den Bereich \[ 0, 1 gebunden \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL. \_ rot**</dt> </dl>                                      | Jedes Element ist eine einzelne rote Komponente. Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Grün und blau und 1,0 für Alpha angefügt werden. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.<br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ grün**</dt> </dl>                                | Jedes Element ist eine einzelne grüne Komponente. Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für "Red" und "Blue" und 1,0 für Alpha angehängt werden. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.<br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ blau**</dt> </dl>                                   | Jedes Element ist eine einzelne blaue Komponente. Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot und grün und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.<br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL- \_ Alpha**</dt> </dl>                                | Jedes Element ist eine einzelne rote Komponente. Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot, grün und blau angefügt wird. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.<br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL. \_ RGB**</dt> </dl>                                      | Jedes Element ist ein RGB-Triple. Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Jedes Element ist ein umfassendes RGBA-Element. Der Wert wird in einen Gleit Komma Wert konvertiert. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.<br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ ext**</dt> </dl>                         | Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL \_ BGR \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ ext**</dt> </dl>                      | Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha. GL \_ BGRA \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL- \_ Beleuchtung**</dt> </dl>                    | Jedes Element ist ein einzelner Wert für die Leuchtkraft. Sie wird in Gleit Komma Zahlen konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft dreimal für Rot, grün und blau replizieren und 1,0 für Alpha angefügt wird. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.<br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL- \_ Leuchtkraft \_ Alpha**</dt> </dl> | Jedes Element ist ein leuchtendes/Alpha-Paar. Sie wird in den Gleit Komma Wert konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft drei Mal für Rot, grün und blau replizieren wird. Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.<br/>                                                                                                                                                 |



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der Pixeldaten. Die folgenden symbolischen Werte werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.

</dd> <dt>

*Pixel* 
</dt> <dd>

Ein Zeiger auf die Bilddaten im Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* war keine GL \_ \_ -Textur 2D.<br/>                                                                                                                                                                                |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Format* war keine akzeptierte *Format* Konstante. Nur Format Konstanten außer dem GL \_ -Schablonen \_ Index und der GL- \_ tiefen \_ Komponente werden akzeptiert. Eine Liste möglicher Werte finden Sie in der Beschreibung des- *Formats* des-Parameters.<br/> |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Typ* war keine *typkonstante* .<br/>                                                                                                                                                                                   |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Typ* : GL \_ Bitmap und *Format* war kein GL \_ - \_ Farbindex.<br/>                                                                                                                                                        |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size war.<br/>                                                                                                |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *internalformat* war nicht 1, 2, 3 oder 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Breite* oder Höhe war kleiner als 0 (null) oder größer als 2 + gl \_ . die maximale \_ Textur \_ Größe, oder Sie konnte nicht als 2 *n* + 2 (Rahmen) für einen ganzzahligen Wert von *n* dargestellt werden.<br/>                                                  |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | der *Rahmen war nicht* 0 oder 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                                                          |



## <a name="remarks"></a>Bemerkungen

Die **glTexImage2D** -Funktion gibt ein zweidimensionales Textur Bild an. Bei der Texturierung wird ein Teil eines angegebenen *Textur Bilds* allen grafischen Primitiven zugeordnet, für die die Texturierung aktiviert ist. Die zweidimensionale Texturierung wird mithilfe von [**glEnable**](glenable.md) und **glEnable** mit dem Argument GL \_ Texture \_ 2D aktiviert und deaktiviert.

Textur Bilder werden mit **glTexImage2D** definiert. Die Argumente beschreiben die Parameter des Textur Bilds, z. b. Höhe, Breite, Breite des Rahmens, Detailebene (siehe [**gltexparameter**](gltexparameter-functions.md)) und Anzahl der angegebenen Farbkomponenten. Die letzten drei Argumente beschreiben die Darstellung des Bilds im Arbeitsspeicher. Diese Argumente sind identisch mit den für [**gldrawpixels**](gldrawpixels.md)verwendeten Pixel Formaten.

Daten werden je nach *Typ* aus *Pixel* als Sequenz von Bytes mit oder ohne Vorzeichen, Shorts oder Longs oder Gleit Komma Werten mit einfacher Genauigkeit gelesen. Diese Werte werden je nach *Format* in Mengen von einem, zwei, drei oder vier Werten gruppiert, um Elemente zu bilden. Wenn der *Typ* "GL \_ Bitmap" ist, werden die Daten als Zeichenfolge nicht signierter Bytes betrachtet (und das *Format* muss ein GL- \_ \_ Farbindex sein). Jedes Daten Byte wird als 8 1-Bit-Elemente behandelt, wobei die bitanordnung zuerst von GL \_ Entpack- \_ lsb \_ (siehe [**glpixelstore**](glpixelstore-functions.md)) bestimmt wird. Eine Beschreibung der zulässigen Werte für den *Typparameter* finden Sie unter [**gldrawpixels**](gldrawpixels.md) .

Ein Textur Bild kann je nach *Komponenten* bis zu vier Komponenten pro Textur Element aufweisen. Ein Textur Bild mit einer Komponente verwendet nur die rote Komponente der aus *Pixel* extrahierten RGBA-Farbe. Ein Image mit zwei Komponenten verwendet den R-Wert und einen-Wert. Ein Image mit drei Komponenten verwendet die Werte R, G und B. Ein Image mit vier Komponenten verwendet alle RGBA-Komponenten.

Die Texturierung hat keine Auswirkung auf den Farb Index Modus.

Das Textur Bild kann mit den gleichen Datenformaten dargestellt werden wie die Pixel in einem **gldrawpixels** -Befehl, mit dem Unterschied, dass der GL \_ \_ -Schablone-Index und die GL- \_ tiefen \_ Komponente nicht verwendet werden können. Die [**glpixelstore**](glpixelstore-functions.md) -und [**glpixeltransfer**](glpixeltransfer.md) -Modi wirken sich auf Textur Bilder genau so aus, wie Sie sich auf **gldrawpixels** auswirken.

Ein Textur Bild, bei dem die Höhe oder Breite null ist, gibt die NULL-Textur an Wenn die NULL-Textur für die Detailebene 0 angegeben wird, ist dies so, als ob die Texturierung deaktiviert wäre.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexImage2D** ab:

[**glgetteximage**](glgetteximage.md)

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D

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

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glnebel**](glfog.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**gltexd**](gltexenv-functions.md)
</dt> <dt>

[**gltexgen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





