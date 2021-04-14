---
title: glread Pixels-Funktion (GL. h)
description: Die gllesepixels-Funktion liest einen Block von Pixeln aus dem Framebuffer.
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- glread Pixels-Funktion OpenGL
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
ms.openlocfilehash: a853d67be282227168da4b90f4fdd47a49d2d212
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391539"
---
# <a name="glreadpixels-function"></a>glread Pixels-Funktion

Die **gllesepixels** -Funktion liest einen Block von Pixeln aus dem Framebuffer.

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

Die Fenster *x* -Koordinate des ersten Pixels, das aus dem Framebuffer gelesen wird. Gibt in Verbindung mit der *y* -Koordinate die Position der unteren linken Ecke eines rechteckigen Blocks von Pixeln an.

</dd> <dt>

*y* 
</dt> <dd>

Die Fenster- *y* -Koordinaten des ersten Pixels, das aus dem Framebuffer gelesen wird. Gibt in Verbindung mit der *x* -Koordinate die Position der unteren linken Ecke eines rechteckigen Blocks von Pixeln an.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Pixel Rechtecks.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Pixel Rechtecks. Die *Width* -und *height* -Parameter des Werts "1" entsprechen einem einzelnen Pixel.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden symbolischen Werte werden akzeptiert:



| Wert                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL- \_ Farb \_ Index**</dt> </dl>                                                                                                                                                                                                                                                                                                               | Farbindizes werden aus dem Farb Puffer gelesen, der von [**gllesebuffer**](glreadbuffer.md)ausgewählt wird. Jeder Index wird je nach Wert und Vorzeichen der GL-Index Verschiebung in einen Fixed-Punkt konvertiert, nach links oder rechts verschoben \_ \_ und dem GL- \_ Index Offset hinzugefügt \_ . Wenn die GL- \_ Karten \_ Farbe "GL true" ist \_ , werden Indizes durch ihre Zuordnungen in der Tabelle "GL \_ Pixel \_ map i" ersetzt \_ \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt>**GL- \_ Schablonen \_ Index**</dt> </dl>                                                                                                                                                                                                                                                                                                         | Schablonen Werte werden aus dem Schablonen Puffer gelesen. Jeder Index wird je nach Wert und Vorzeichen der GL-Index Verschiebung in einen Fixed-Punkt konvertiert, nach links oder rechts verschoben \_ \_ und dem GL- \_ Index Offset hinzugefügt \_ . Wenn die GL- \_ Karten \_ Schablone "GL true" ist \_ , werden Indizes durch ihre Zuordnungen in der Tabelle "GL \_ Pixel \_ map s" zu "" ersetzt \_ \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt>**GL- \_ tiefen \_ Komponente**</dt> </dl>                                                                                                                                                                                                                                                                                                   | Tiefen Werte werden aus dem tiefen Puffer gelesen. Jede Komponente wird in einen Gleit Komma Wert konvertiert, sodass der minimale tiefen Wert 0,0 und der Höchstwert 1,0 zugeordnet wird. Die einzelnen Komponenten werden dann mit \_ der tiefen Skala von GL multipliziert \_ , dem GL \_ -tiefen Bias hinzugefügt \_ und schließlich an den Bereich \[ 0, 1 gebunden \] .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <dt>**GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance, GL \_ Luminance \_ Alpha**</dt> </dl> | Die Verarbeitung unterscheidet sich abhängig davon, ob Farb Puffer Farbindizes oder RGBA-Farbkomponenten speichern. Wenn Farbindizes gespeichert werden, werden Sie aus dem von [**gllesebuffer**](glreadbuffer.md)ausgewählten Farb Puffer gelesen. Jeder Index wird je nach Wert und Vorzeichen der GL-Index Verschiebung in einen Fixed-Punkt konvertiert, nach links oder rechts verschoben \_ \_ und dem GL- \_ Index Offset hinzugefügt \_ . Indizes werden dann durch die roten, grünen, blauen und Alpha-Werte ersetzt, die durch Indizierung von GL \_ Pixel \_ map \_ i \_ zu \_ R, GL \_ Pixel \_ map \_ i \_ zu \_ G, GL \_ Pixel Map i zu \_ \_ \_ \_ B und GL \_ Pixel \_ map \_ i \_ zu \_ a Tables abgerufen werden. Wenn RGBA Color-Komponenten in den Farb Puffern gespeichert werden, werden Sie aus dem durch **gllebuffer** ausgewählten Farb Puffer gelesen. Jede Farbkomponente wird in einen Gleit Komma Wert konvertiert, sodass die NULL-Intensität 0,0 und die vollständige Intensität 1,0 zugeordnet wird. Jede Komponente wird dann mit der Skala von GL \_ c multipliziert \_ und zu GL c-Bias hinzugefügt \_ \_ , wobei c der Wert von GL \_ red, GL \_ Green, GL \_ Blue und GL \_ Alpha ist. Jede Komponente wird an den Bereich \[ 0, 1 gebunden \] . Wenn die GL- \_ Karten \_ Farbe GL \_ true ist, wird jede Farbkomponente c durch ihre Zuordnung in der Tabelle GL \_ Pixel \_ map \_ c \_ zu c ersetzt \_ , wobei c wiederum GL \_ red, GL \_ Green, GL \_ Blue und GL Alpha ist \_ . Jede Komponente wird auf die Größe der entsprechenden Tabelle skaliert, bevor die Suche durchgeführt wird. Zum Schluss werden nicht benötigte Daten verworfen. Beispielsweise \_ verwirft GL Red die grün-, blau-und Alpha Komponenten, während GL \_ RGB nur die Alpha Komponente verwirft. GL \_ Luminance berechnet einen einzelnen Komponenten Wert als Summe der roten, grünen und blauen Komponenten, und GL \_ Luminance \_ Alpha führt den gleichen Wert aus, während Alpha als zweiter Wert beibehalten wird.<br/> |



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp der Pixeldaten. Muss einen der folgenden Werte aufweisen.



| type                | Index Maske | Komponenten Konvertierung |
|---------------------|------------|----------------------|
| GL- \_ Byte ohne Vorzeichen \_  | 281        | (281) *c*             |
| GL \_ Byte            | 271        | \[(271) *c*-1 \] /2     |
| GL- \_ Bitmap          | 1          | 1                    |
| GL \_ unsigned \_ Short | 2 61       | (2 61) *c*            |
| GL \_ Short           | 2 51       | \[(2 51) *c* 1 \] /2     |
| GL \_ unsigned \_ int\_ | 2 1       | (2 1) *c*            |
| GL \_ int             | 2 1      | \[(2 1) *c* 1 \] /2     |
| GL \_ float           | none       | *c*                  |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Gibt die Pixeldaten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Format* oder *Typ* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Format* war \_ der GL \_ -Farbindex, und die Farb Puffer gespeicherten RGBA-oder BGRA-Farbkomponenten.<br/>                                 |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Format* war der GL \_ \_ -Schablone-Index, und es gab keinen Schablonen Puffer.<br/>                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Das *Format* war \_ eine GL \_ -tiefen Komponente, und es gab keinen tiefen Puffer.<br/>                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gllepixels** " gibt Pixeldaten aus dem Framebuffer zurück, beginnend mit dem Pixel, dessen untere linke Ecke sich am Speicherort (*x*, *y*) befindet, beginnend mit dem Speicherort *Pixel* in Client Speicher. Mehrere Parameter steuern die Verarbeitung der Pixeldaten, bevor Sie in den Client Speicher eingefügt werden. Diese Parameter werden mit drei Befehlen festgelegt: " [**glpixelstore**](glpixelstore-functions.md)", " [**glpixeltransfer**](glpixeltransfer.md)" und " [**glpixelmap**](glpixelmap.md)". In diesem Thema werden die Auswirkungen auf **glread Pixel** der meisten, aber nicht alle Parameter beschrieben, die durch diese drei Befehle angegeben werden.

Die **glread Pixels** -Funktion gibt Werte von jedem Pixel mit der unteren linken Ecke bei (*x* + i, *y* + j) für 0 = i < *Width* und 0 = j < *Höhe* zurück. Dieses Pixel ist das *i*. Pixel in der Zeile *j*. Pixel werden in Zeilen Reihenfolge von der niedrigsten zur höchsten Zeile (von links nach rechts) in jeder Zeile zurückgegeben.

Die oben beschriebenen Shift-, Scale-, Bias-und Suche-Faktoren werden von [**glpixeltransfer**](glpixeltransfer.md)angegeben. Der Inhalt der Nachschlage Tabelle wird von [**glpixelmap**](glpixelmap.md)angegeben.

Der letzte Schritt umfasst das umrechnen der Indizes oder Komponenten in das richtige Format, wie durch den *Typ* angegeben. Wenn *Format* der Wert "GL \_ Color \_ Index" oder "GL \_ Stencil Index" lautet \_ und der *Typ* nicht "GL float" ist \_ , wird jeder Index mit dem in der folgenden Tabelle angegebenen Maskenwert maskiert. Wenn der *Typ* "GL float" ist \_ , wird jeder ganzzahlige Index in ein Gleit Komma Format mit einfacher Genauigkeit konvertiert.

Wenn *Format* GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ Alpha und *Type* ist nicht gl \_ float, wird jede Komponente mit dem in der obigen Tabelle gezeigten Multiplikator multipliziert. Wenn der Typ "GL float" ist \_ , wird jede Komponente unverändert (oder in das Gleit Komma Format mit einfacher Genauigkeit des Clients konvertiert, wenn Sie sich von der von OpenGL verwendeten unterscheidet).

Rückgabewerte werden wie folgt in den Arbeitsspeicher eingefügt. Wenn *Format* die Werte "GL \_ Color \_ Index", "GL \_ Stencil \_ Index", "GL- \_ tiefen Komponente", " \_ GL Red", " \_ GL Green", " \_ GL Blue", "GL Alpha" oder " \_ \_ GL Luminance" ist, wird \_ ein einzelner Wert zurück gegeben,und die Daten für das *i* Th-Pixel in der *j*  +   GL \_ RGB und GL \_ BGR \_ ext geben drei Werte zurück: GL \_ RGBA und GL \_ BGRA \_ ext geben vier Werte zurück, und GL \_ Luminance \_ alpha gibt zwei Werte für jedes Pixel zurück, wobei alle Werte einem einzelnen Pixel entsprechen, das zusammenhängenden Raum in *Pixel* belegt. Von [**glpixelstore**](glpixelstore-functions.md)festgelegte Speicher Parameter, wie z. b. "GL \_ Pack \_ Swap \_ Bytes" und "GL \_ Pack \_ lsb First" \_ , wirken sich darauf aus, wie Daten in den Arbeitsspeicher geschrieben Eine Beschreibung finden Sie unter [**glpixelstore**](glpixelstore-functions.md) .

Werte für Pixel, die außerhalb des Fensters liegen, das mit dem aktuellen OpenGL-Kontext verbunden ist, sind nicht definiert.

Wenn ein Fehler generiert wird, wird keine Änderung an dem Inhalt der *Pixel* vorgenommen.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glread Pixel** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Index \_ Modus

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glpixelmap**](glpixelmap.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glread Buffer**](glreadbuffer.md)
</dt> </dl>

 

 





