---
title: glReadPixels-Funktion (Gl.h)
description: Die glReadPixels-Funktion liest einen Pixelblock aus dem Framepuffer.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- glReadPixels-Funktion OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03a90fcd6ee5179a900739c40e78f796c6340d9609f4cfbeb21e6a70156afe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937940"
---
# <a name="glreadpixels-function"></a>glReadPixels-Funktion

Die **glReadPixels-Funktion** liest einen Pixelblock aus dem Framepuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die  Fenster x-Koordinate des ersten Pixels, das aus dem Framepuffer gelesen wird. Gibt zusammen  mit der y-Koordinate die Position der unteren linken Ecke eines rechteckigen Pixels an.

</dd> <dt>

*y* 
</dt> <dd>

Die *Fenster-y-Koordinaten* des ersten Pixels, das aus dem Framepuffer gelesen wird. Gibt zusammen  mit der x-Koordinate die Position der unteren linken Ecke eines rechteckigen Pixels an.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Pixelrechtecks.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Pixelrechtecks. *Breiten-* und *Höhenparameter* des Werts "1" entsprechen einem einzelnen Pixel.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden symbolischen Werte werden akzeptiert:



| Wert                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Farbindizes werden aus dem von [**glReadBuffer**](glreadbuffer.md)ausgewählten Farbpuffer gelesen. Jeder Index wird in einen festen Punkt konvertiert, je nach Wert und Vorzeichen von GL INDEX SHIFT nach links oder rechts verschoben \_ und zu GL INDEX OFFSET \_ \_ \_ hinzugefügt. Wenn GL \_ MAP COLOR GL TRUE \_ \_ ist, werden Indizes durch ihre Zuordnungen in der Tabelle GL \_ PIXEL MAP I TO I \_ \_ \_ \_ ersetzt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**GL \_ STENCIL \_ INDEX**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Schablonenwerte werden aus dem Schablonenpuffer gelesen. Jeder Index wird in einen festen Punkt konvertiert, je nach Wert und Vorzeichen von GL INDEX SHIFT nach links oder rechts verschoben \_ und zu GL INDEX OFFSET \_ \_ \_ hinzugefügt. Wenn GL \_ MAP \_ STENCIL GL \_ TRUE ist, werden Indizes durch ihre Zuordnungen in der Tabelle GL \_ PIXEL MAP S TO S \_ \_ \_ \_ ersetzt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**GL \_ DEPTH \_ COMPONENT**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Tiefenwerte werden aus dem Tiefenpuffer gelesen. Jede Komponente wird in Gleitkommawerte konvertiert, sodass der Mindesttiefewert 0,0 und der maximale Wert 1,0 zugeordnet wird. Jede Komponente wird dann mit GL \_ DEPTH \_ SCALE multipliziert, zu GL DEPTH BIAS hinzugefügt \_ und schließlich an den Bereich \_ \[ 0,1 \] gebunden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE, GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Die Verarbeitung unterscheidet sich je nachdem, ob Farbpuffer Farbindizes oder RGBA-Farbkomponenten speichern. Wenn Farbindizes gespeichert werden, werden sie aus dem von [**glReadBuffer**](glreadbuffer.md)ausgewählten Farbpuffer gelesen. Jeder Index wird in einen festen Punkt konvertiert, je nach Wert und Vorzeichen von GL INDEX SHIFT nach links oder rechts verschoben \_ und zu GL INDEX OFFSET \_ \_ \_ hinzugefügt. Indizes werden dann durch die Rot-, Grün-, Blau- und Alphawerte ersetzt, die durch Indizieren der Tabellen GL \_ PIXEL MAP I TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ \_ G, GL PIXEL MAP I TO B und GL PIXEL MAP I TO \_ A \_ \_ \_ \_ \_ \_ \_ \_ \_ abgerufen werden. Wenn RGBA-Farbkomponenten in den Farbpuffern gespeichert werden, werden sie aus dem von **glReadBuffer** ausgewählten Farbpuffer gelesen. Jede Farbkomponente wird in Gleitkomma konvertiert, sodass die Intensität 0,0 und die vollständige Intensität 1,0 entspricht. Jede Komponente wird dann mit GL c SCALE multipliziert \_ und gl c BIAS \_ \_ \_ hinzugefügt, wobei c GL \_ RED, GL \_ GREEN, GL BLUE und GL \_ ALPHA \_ ist. Jede Komponente ist an den Bereich \[ 0,1 angeklammert. \] Wenn GL \_ MAP \_ COLOR GL TRUE \_ ist, wird jede Farbkomponente c durch ihre Zuordnung in der Tabelle GL \_ PIXEL MAP c TO c \_ \_ \_ \_ ersetzt, wobei c wieder GL \_ RED, GL \_ GREEN, GL BLUE und GL ALPHA \_ \_ ist. Jede Komponente wird auf die Größe ihrer entsprechenden Tabelle skaliert, bevor die Suche ausgeführt wird. Schließlich werden nicht benötigte Daten verworfen. Gl RED \_ verwirft beispielsweise die Grün-, Blau- und Alphakomponenten, während GL \_ RGB nur die Alphakomponente verwirft. GL \_ LUMINANCE berechnet einen einzelnen Komponentenwert als Summe der roten, grünen und blauen Komponenten, und GL \_ LUMINANCE \_ ALPHA macht den gleichen Wert, während alpha als zweiter Wert bleibt.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der Pixeldaten. Dabei muss es sich um einen der folgenden Werte handeln.



| type                | Indexmaske | Komponentenkonvertierung |
|---------------------|------------|----------------------|
| GL \_ UNSIGNED \_ BYTE  | 281        | (281) *c*             |
| GL \_ BYTE            | 271        | \[(271) *c*-1 \] /2     |
| GL \_ BITMAP          | 1          | 1                    |
| GL \_ UNSIGNED \_ SHORT | 2 61       | (2 61) *c*            |
| GL \_ SHORT           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ UNSIGNED \_ INT\_ | 2 1       | (2 1) *c*            |
| GL \_ INT             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ FLOAT           | Keine       | *c*                  |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Gibt die Pixeldaten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* oder *type* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                   |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Das Format* lautete GL \_ COLOR \_ INDEX, und die Farbpuffer speicherten RGBA- oder BGRA-Farbkomponenten.<br/>                                 |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Format* war GL \_ STENCIL \_ INDEX, und es gab keinen Schablonenpuffer.<br/>                                                          |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Format:* GL \_ DEPTH \_ COMPONENT, und es gab keinen Tiefenpuffer.<br/>                                                          |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |

## <a name="remarks"></a>Hinweise

Die **glReadPixels-Funktion** gibt Pixeldaten aus dem Framepuffer zurück, beginnend mit dem Pixel, dessen untere linke Ecke sich an der Position (*x*, *y*) befindet, in den Clientspeicher, beginnend bei den *Speicherortpixeln.* Mehrere Parameter steuern die Verarbeitung der Pixeldaten, bevor sie in den Clientspeicher platziert werden. Diese Parameter werden mit drei Befehlen festgelegt: [**glPixelStore,**](glpixelstore-functions.md) [**glPixelTransfer**](glpixeltransfer.md)und [**glPixelMap.**](glpixelmap.md) In diesem Thema werden die Auswirkungen auf **glReadPixels** der meisten, aber nicht aller Parameter beschrieben, die von diesen drei Befehlen angegeben werden.

Die **glReadPixels-Funktion** gibt Werte von jedem Pixel mit der unteren linken Ecke an (*x* + i, *y* + j) für 0 = i < *Breite* und 0 = j < *Höhe* zurück. Dieses Pixel wird als das i-th-Pixel in der *j-ten* Zeile bezeichnet.  Pixel werden in Zeilenreihenfolge von der untersten bis zur höchsten Zeile von links nach rechts in jeder Zeile zurückgegeben.

Die oben beschriebenen Verschiebungs-, Skalierungs-, Verzerrungs- und Suchfaktoren werden alle durch [**glPixelTransfer**](glpixeltransfer.md)angegeben. Der Inhalt des Nachschlagetabellenverzeichnisses wird von [**glPixelMap**](glpixelmap.md)angegeben.

Der letzte Schritt umfasst die Konvertierung der Indizes oder Komponenten in das richtige Format, wie vom *Typ* angegeben. Wenn *das Format* GL COLOR INDEX oder GL \_ \_ \_ STENCIL \_ INDEX ist und der *Typ* nicht GL \_ FLOAT ist, wird jeder Index mit dem mask-Wert maskiert, der in der folgenden Tabelle angegeben ist. Wenn *der Typ* GL FLOAT \_ ist, wird jeder ganzzahlige Index in ein Gleitkommaformat mit einfacher Genauigkeit konvertiert.

Wenn *das Format* GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE oder GL \_ LUMINANCE \_ ALPHA lautet und der *Typ* nicht GL \_ FLOAT ist, wird jede Komponente mit dem in der obigen Tabelle dargestellten Multiplikator multipliziert. Wenn der Typ GL \_ FLOAT ist, wird jede Komponente wie besehen übergeben (oder in das Gleitkommaformat mit einfacher Genauigkeit des Clients konvertiert, wenn sie sich von dem von OpenGL verwendeten unterscheidet).

Rückgabewerte werden wie folgt im Arbeitsspeicher platziert. Wenn *das Format* "GL COLOR \_ \_ INDEX", "GL \_ STENCIL \_ INDEX", "GL \_ DEPTH \_ COMPONENT", "GL \_ RED", "GL \_ GREEN", "GL \_ BLUE", "GL \_ ALPHA" oder "GL \_ LUMINANCE" lautet, wird ein einzelner Wert zurückgegeben, und die Daten für das *i-ten* Pixel in der j.th-Zeile werden an position (*j* )*width*   +  *i* platziert. GL \_ RGB und GL \_ BGR EXT geben drei Werte \_ zurück, GL \_ RGBA und GL \_ BGRA EXT geben vier Werte \_ zurück, und GL \_ LUMINANCE \_ ALPHA gibt zwei Werte für jedes Pixel zurück, wobei alle Werte einem einzelnen Pixel entsprechen, das zusammenhängenden Raum in *Pixel* belegt. Storage parameter, die von [**glPixelStore**](glpixelstore-functions.md)festgelegt werden, z. B. GL \_ PACK SWAP BYTES und GL PACK \_ \_ \_ \_ LSB \_ FIRST, beeinflussen die Art und Weise, wie Daten in den Arbeitsspeicher geschrieben werden. Eine Beschreibung finden Sie unter [**glPixelStore.**](glpixelstore-functions.md)

Werte für Pixel, die sich außerhalb des Fensters befinden, das mit dem aktuellen OpenGL-Kontext verbunden ist, sind nicht definiert.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *Pixeln* vorgenommen.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glReadPixels ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ INDEX \_ MODE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





