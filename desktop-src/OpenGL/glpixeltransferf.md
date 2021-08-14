---
title: glPixelTransferf-Funktion (Gl.h)
description: Die Funktionen glPixelTransferf und glPixelTransferi legen die Pixelübertragungsmodi fest. | glPixelTransferf-Funktion (Gl.h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- glPixelTransferf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2268147511a40aaf70a928c77b177f76870e65a7f40da4f2c6bf9428f67db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358570"
---
# <a name="glpixeltransferf-function"></a>glPixelTransferf-Funktion

Die Funktionen **glPixelTransferf** und [**glPixelTransferi**](glpixeltransferi.md) legen die Pixelübertragungsmodi fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Der symbolische Name des festzulegenden Pixelübertragungsparameters. Die folgende Tabelle enthält den Typ, den Anfangswert und den Bereich der gültigen Werte für jeden der Pixelübertragungsparameter, die mit **glPixelTransfer** festgelegt sind.



| Pname             | type    | Anfangswert  | Gültiger Bereich  |
|-------------------|---------|----------------|--------------|
| GL \_ MAP \_ COLOR    | Boolean | false          | TRUE/FALSE   |
| GL \_ MAP \_ STENCIL  | Boolean | false          | TRUE/FALSE   |
| GL \_ INDEX \_ SHIFT  | integer | 0              | (8,8)        |
| GL \_ INDEX \_ OFFSET | integer | 0              | (8,8)        |
| GL \_ RED \_ SCALE    | integer | 1.0            | (8,8)        |
| GL \_ GREEN \_ SCALE  | float   | 1.0            | (8,8)        |
| GL \_ BLUE \_ SCALE   | float   | 1.0            | (8,8)        |
| GL \_ ALPHA \_ SCALE  | float   | 1.0            | (8,8)        |
| \_ \_ GL-TIEFENSKALA  | float   | 1.0            | (8,8)        |
| GL \_ RED \_ BIAS     | float   | 0,0            | (8,8)        |
| GL \_ GREEN \_ BIAS   | float   | 0,0            | (8,8)        |
| GL \_ BLUE \_ BIAS    | float   | 0,0            | (8,8)        |
| GL \_ ALPHA \_ BIAS   | float   | 0,0            | (8,8)        |
| GL \_ DEPTH \_ BIAS   | float   | 0,0            | (8,8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *pname* festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glPixelTransfer-Funktion** legt Pixelübertragungsmodi fest, die sich auf den Betrieb der nachfolgenden [**Befehle glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [](glcopytexsubimage2d.md) [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md) auswirken. Die von den Pixelübertragungsmodi angegebenen Algorithmen arbeiten mit Pixeln, nachdem sie aus dem Framepuffer (**glReadPixels** und **glCopyPixels**) gelesen oder aus dem Clientspeicher entpackt wurden (**glDrawPixels**, **glTexImage1D** und **glTexImage2D**). Pixelübertragungsvorgänge erfolgen in der gleichen Reihenfolge und auf die gleiche Weise, unabhängig vom Befehl, der zum Pixelvorgang geführt hat. Die Pixelspeichermodi [**(glPixelStore)**](glpixelstore-functions.md)steuern das Entpacken von Pixeln, die aus dem Clientspeicher gelesen werden, und die Komprimierung von Pixeln, die wieder in den Clientspeicher geschrieben werden.

Pixelübertragungsvorgänge verarbeiten vier grundlegende Pixeltypen: *Farbe,* *Farbindex,* *Tiefe* und *Schablone*. Farbpixel bestehen aus vier Gleitkommawerten mit nicht angegebenen Mantisse- und Exponentengrößen, skaliert so, dass 0,0 die Intensität null und 1,0 die vollständige Intensität darstellt. Farbindizes bestehen aus einem einzelnen Festkommawert mit nicht angegebener Genauigkeit rechts vom Binärpunkt. Tiefenpixel umfassen einen einzelnen Gleitkommawert mit nicht angegebenen Mantisse- und Exponentengrößen, skaliert so, dass 0,0 den Minimalwert des Tiefenpuffers und 1,0 den maximalen Tiefenpufferwert darstellt. Schließlich bestehen Schablonenpixel aus einem einzelnen Festkommawert mit nicht angegebener Genauigkeit rechts vom Binärpunkt.

Die Pixelübertragungsvorgänge, die für die vier grundlegenden Pixeltypen ausgeführt werden, sind wie folgt:



| Pixeltyp  | Pixelübertragungsvorgang                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Jede der vier Farbkomponenten wird mit einem Skalierungsfaktor multipliziert und dann einem Verzerrungsfaktor hinzugefügt. Das heißt, die rote Komponente wird mit GL RED SCALE multipliziert \_ und dann GL RED BIAS \_ \_ \_ hinzugefügt. Die grüne Komponente wird mit GL GREEN SCALE multipliziert \_ und dann zu GL GREEN BIAS \_ \_ \_ hinzugefügt. Die blaue Komponente wird mit GL BLUE SCALE multipliziert \_ und dann GL BLUE BIAS \_ \_ \_ hinzugefügt. Die Alphakomponente wird mit GL ALPHA SCALE multipliziert \_ und dann zu GL ALPHA BIAS \_ \_ \_ hinzugefügt. Nachdem alle vier Farbkomponenten skaliert und voreingenommen sind, wird jede an den Bereich \[ 0,1 \] klammern. Alle Farbskala- und Verzerrungswerte werden mit **glPixelTransfer** angegeben. <br/> Wenn GL \_ MAP \_ COLOR true ist, wird jede Farbkomponente durch die Größe der entsprechenden Farbzuordnung skaliert und dann durch den Inhalt dieser Karte ersetzt, die von der skalierten Komponente indiziert wird. Das heißt, die rote Komponente wird von GL PIXEL MAP R TO R SIZE skaliert und dann durch den Inhalt von GL PIXEL MAP R TO R selbst \_ \_ \_ indiziert \_ \_ \_ \_ \_ \_ \_ \_ ersetzt. Die grüne Komponente wird von GL PIXEL MAP G TO G SIZE skaliert \_ und dann durch den Inhalt von GL PIXEL MAP \_ G TO \_ G automatisch \_ indiziert \_ \_ \_ \_ \_ \_ \_ ersetzt. Die blaue Komponente wird von GL PIXEL MAP B TO B SIZE skaliert \_ und dann durch den Inhalt von GL PIXEL MAP \_ B TO \_ B automatisch \_ indiziert \_ \_ \_ \_ \_ \_ \_ ersetzt. Die Alphakomponente wird von GL PIXEL MAP A TO A SIZE skaliert \_ und dann durch den Inhalt von GL PIXEL MAP A TO A ersetzt, die \_ selbst indiziert \_ \_ \_ \_ \_ \_ \_ \_ \_ ist. Alle aus den Karten entnommenen Komponenten werden dann an den Bereich \[ 0,1 \] angerückt. GL \_ MAP COLOR wird mit \_ **glPixelTransfer** angegeben. Der Inhalt der verschiedenen Zuordnungen wird mit **glPixelMap** angegeben.<br/>                                                                                                                        |
| Farbindex | Jeder Farbindex wird durch GL INDEX SHIFT-Bits nach links verschoben und füllt alle Bits mit Nullen auf, die über die Anzahl der Bruchbits hinausgehen, die vom \_ \_ Festpunktindex aufgenommen werden. Wenn GL \_ INDEX \_ SHIFT negativ ist, wird die Verschiebung nach rechts und wieder null ausgefüllt. GL \_ INDEX OFFSET wird dann dem Index \_ hinzugefügt. GL \_ INDEX SHIFT und GL INDEX OFFSET werden mit \_ \_ \_ **glPixelTransfer angegeben.**<br/> Ab diesem Punkt weicht der Vorgang abhängig vom erforderlichen Format der resultierenden Pixel ab. Wenn die resultierenden Pixel in einen Farbindexpuffer geschrieben werden sollen oder wenn sie im GL COLOR INDEX-Format in den Clientspeicher zurückgelesen werden, werden die Pixel weiterhin als \_ \_ Indizes behandelt. Wenn GL MAP COLOR true ist, wird jeder Index durch \_ \_ 2 ^ *n* 1 maskiert, wobei *n* GL \_ PIXEL MAP I TO I SIZE ist, und dann durch den Inhalt von GL PIXEL MAP I TO I indiziert durch den maskierten Wert \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ ersetzt. GL \_ MAP COLOR wird mit \_ **glPixelTransfer angegeben.** Der Inhalt der Indexzuordnung wird mit **glPixelMap angegeben.**<br/> Wenn die resultierenden Pixel in einen RGBA-Farbpuffer geschrieben werden sollen oder in einem anderen Format als GL COLOR INDEX in den Clientspeicher zurückgelesen werden, werden die Pixel von Indizes in Farben konvertiert, indem auf die vier Karten \_ GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B und \_ GL \_ PIXEL MAP I TO \_ \_ \_ A \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ verweisen. Vor dem Dereferenzieren wird der Index durch 2 n 1 maskiert, wobei n GL PIXEL MAP I TO R SIZE für die rote Karte, GL PIXEL MAP I TO G SIZE für die grüne Karte, GL PIXEL MAP I TO B SIZE für die blaue Karte und \_ \_ \_ GL \_ \_ \_ PIXEL MAP I \_ TO \_ \_ A \_ SIZE für \_ \_ \_ \_ die \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Alphakarte ist. Alle Komponenten aus den Zuordnungen werden dann an den Bereich \[ 0,1 geklammert. \] Der Inhalt der vier Zuordnungen wird mit **glPixelMap angegeben.**<br/> |
| Tiefe       | Jeder Tiefenwert wird mit GL DEPTH SCALE multipliziert, gl depth bias hinzugefügt und dann an den Bereich \_ \_ \_ \_ \[ 0,1 \] angefügt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Jeder Index wird in GL INDEX SHIFT-Bits genau wie ein Farbindex verschoben und dann \_ \_ GL INDEX OFFSET \_ \_ hinzugefügt. Wenn GL MAP STENCIL true ist, wird jeder Index durch \_ \_ 2n 1 maskiert, wobei *n* GL \_ PIXEL MAP S TO S SIZE ist, und dann durch den Inhalt von GL PIXEL MAP S TO S ersetzt, indiziert durch den maskierten \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Wert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Die [**glPixelTransferf-Funktion**](glpixeltransfer.md) kann zum Festlegen beliebiger Pixelübertragungsparameter verwendet werden. Wenn der Parametertyp boolesch ist, impliziert 0.0 false, und jeder andere Wert impliziert TRUE. Wenn *pname ein* ganzzahliger Parameter ist, *wird der Parameter* auf die nächste ganze Zahl gerundet.

Ebenso kann **glPixelTransferi auch zum** Festlegen aller Pixelübertragungsparameter verwendet werden. Boolesche Parameter werden auf FALSE festgelegt, *wenn param* 0 und andernfalls TRUE ist. Der *Parameter param* wird in einen Gleitkomma konvertiert, bevor er echten Parametern zugewiesen wird.

Wenn ein [**glDrawPixels-,**](gldrawpixels.md) [**glReadPixels-,**](glreadpixels.md) [**glCopyPixels-,**](glcopypixels.md) [**glTexImage1D-**](glteximage1d.md)oder [**glTexImage2D-Befehl**](glteximage2d.md) in einer Anzeigeliste platziert wird (siehe [**glNewList**](glnewlist.md) und [**glCallList),**](glcalllist.md)werden die Einstellungen für den Pixelübertragungsmodus verwendet, wenn die Anzeigeliste ausgeführt wird.  Sie können sich von den Einstellungen unterscheiden, die beim Kompilieren des Befehls in die Anzeigeliste verwendet wurden.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPixelTransfer ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAP \_ COLOR

**glGet** mit Argument GL \_ MAP \_ STENCIL

**glGet** mit argument GL \_ INDEX \_ SHIFT

**glGet** mit Argument GL \_ INDEX \_ OFFSET

**glGet** mit Argument GL \_ RED \_ SCALE

**glGet** mit argument GL \_ RED \_ BIAS

**glGet mit** Argument GL \_ GREEN \_ SCALE

**glGet mit** Argument GL \_ GREEN \_ BIAS

**glGet** mit argument GL \_ BLUE \_ SCALE

**glGet mit** argument GL \_ BLUE \_ BIAS

**glGet mit** argument GL \_ ALPHA \_ SCALE

**glGet** mit argument GL \_ ALPHA \_ BIAS

**glGet mit** Argument GL \_ DEPTH \_ SCALE

**glGet** mit Argument GL \_ DEPTH \_ BIAS

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





