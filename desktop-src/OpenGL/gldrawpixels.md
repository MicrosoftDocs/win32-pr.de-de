---
title: glDrawPixels-Funktion (Gl.h)
description: Die glDrawPixels-Funktion schreibt einen Pixelblock in den Framepuffer.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- glDrawPixels-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26546b0c0d8c335f2f741f10d50a7042fffc304ad54be4ed779910fcb84246be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616542"
---
# <a name="gldrawpixels-function"></a>glDrawPixels-Funktion

Die **glDrawPixels-Funktion** schreibt einen Pixelblock in den Framepuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*width* 
</dt> <dd>

Die Breitendimension des Pixelrechtecks, das in den Framepuffer geschrieben wird.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhendimension des Pixelrechtecks, das in den Framepuffer geschrieben wird.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Zulässige symbolische Konstanten sind wie folgt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>Jedes Pixel ist ein einzelner Wert, ein Farbindex. <br/>
<ol>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert jedes Pixel in ein Festpunktformat mit einer nicht angegebenen Anzahl von Bits rechts vom Binärpunkt, unabhängig vom Speicherdatentyp. Gleitkommawerte werden in echte Festkommawerte konvertiert. Die <strong>glDrawPixels-Funktion</strong> konvertiert ganzzahlige Daten mit vorzeichen und ohne Vorzeichen, bei der alle Bruchbits auf 0 (null) festgelegt sind. Die Funktion konvertiert Bitmapdaten entweder in 0.0 oder 1.0.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> verschiebt jeden Festpunktindex um GL_INDEX_SHIFT Bits nach links und fügt ihn GL_INDEX_OFFSET. Wenn GL_INDEX_SHIFT negativ ist, wird nach rechts verschoben. In beiden Fällen füllen 0 Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</li>
<li>Im RGBA-Modus konvertiert <strong>glDrawPixels</strong> den resultierenden Index mithilfe der Tabellen GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B und GL_PIXEL_MAP_I_TO_A RGBA-Pixel. Wenn im Farbindexmodus und GL_MAP_COLOR true ist, wird der Index durch den Wert ersetzt, auf den <strong>glDrawPixels</strong> in der Nachschlagetabelle GL_PIXEL_MAP_I_TO_I.</li>
<li>Unabhängig davon, ob die Ersetzung des Indexes erfolgt oder nicht, ist der ganzzahlige Teil des Indexes <strong>AND</strong>mit 2<sup>b</sup> 1, wobei b die Anzahl der Bits in einem Farbindexpuffer - ist. <em></em></li>
<li>Die resultierenden Indizes oder RGBA-Farben werden dann in Fragmente konvertiert, indem die aktuelle Rasterposition <em>z</em>-koordinate und Texturkoordinaten an jedes Pixel angefügt und dann <em>x-</em> und y-Fensterkoordinaten dem <em></em> <em>n-th-Fragment</em>so zugewiesen werden, dass <em>x</em>? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/width</em><br/> Wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist.<br/></li>
<li>Die <strong>glDrawPixels-Funktion</strong> behandelt diese Pixelfragmente genau wie die Fragmente, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Sie wendet Texturzuordnung, Bruch und alle Fragmentvorgänge an, bevor die Fragmente in den Framepuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Jedes Pixel ist ein einzelner Wert, ein Schablonenindex. <br/>
<ol>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert sie in ein Festpunktformat mit einer nicht angegebenen Anzahl von Bits rechts vom Binärpunkt, unabhängig vom Speicherdatentyp. Gleitkommawerte werden in echte Festkommawerte konvertiert. Die <strong>glDrawPixels-Funktion</strong> konvertiert ganzzahlige Daten mit vorzeichen und ohne Vorzeichen, bei der alle Bruchbits auf 0 (null) festgelegt sind. Bitmapdaten werden entweder in 0.0 oder 1.0 konvertiert.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> verschiebt jeden Festpunktindex um GL_INDEX_SHIFT Bits nach links und fügt ihn GL_INDEX_OFFSET. Wenn GL_INDEX_SHIFT negativ ist, wird nach rechts verschoben. In beiden Fällen füllen 0 Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</li>
<li>Wenn GL_MAP_STENCIL true ist, wird der Index durch den Wert ersetzt, auf den <strong>glDrawPixels</strong> in der Nachschlagetabelle GL_PIXEL_MAP_S_TO_S.</li>
<li>Unabhängig davon, ob die Ersetzung des Indexes erfolgt oder nicht, wird der ganzzahlige Teil des Indexes mit 2<sup>b</sup> 1 und ed, wobei b die Anzahl der Bits im Schablonenpuffer <strong></strong> - ist. <em></em> Die resultierenden Schablonenindizes werden dann in den Schablonenpuffer geschrieben, damit der <em>n-te</em>Index an Speicherort x ? geschrieben <em>wird.</em> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/width</em><br/> Wobei (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) die aktuelle Rasterposition ist. Nur der Pixelbesitztest, der Scissor-Test und die Schablonen-Schreibmaske wirken sich auf diese Schreibvorgänge aus.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Einzeltiefenkomponente. <br/>
<ol>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert Gleitkommadaten direkt in ein internes Gleitkommaformat mit nicht angegebener Genauigkeit. Ganzzahlige Daten mit Vorzeichen werden linear dem internen Gleitkommaformat zugeordnet, damit der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: Der größte ganzzahlige Wert wird 1,0 zugeordnet, 0,0 ist 0.0 zugeordnet.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> multipliziert den resultierenden Gleitkommatiefewert mit GL_DEPTH_SCALE und fügt ihn GL_DEPTH_BIAS. Das Ergebnis wird an den Bereich [0,1] klammert.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert die resultierenden Tiefenkomponenten in Fragmente, indem sie die aktuelle Rasterpositionsfarbe oder den farblichen Index und die Texturkoordinaten an jedes Pixel anfügen und dann <em>x-</em> und y-Fensterkoordinaten dem <em>n-th-Fragment</em> so zuweisen, <em>dass x</em>? <em></em> = <em></em>x<sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n/width</em><br/> Wobei ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist.<br/></li>
<li>Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Die <strong>glDrawPixels-Funktion</strong> wendet Texturzuordnungs-, Textur- und alle Fragmentvorgänge an, bevor die Fragmente in den Framepuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Vier-Komponenten-Gruppe in dieser Reihenfolge: Rot, Grün, Blau, Alpha. <br/>
<ol>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert Gleitkommawerte direkt in ein internes Gleitkommaformat mit nicht angegebener Genauigkeit. Ganzzahlwerte mit Vorzeichen werden linear dem internen Gleitkommaformat zugeordnet, damit der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: Der größte ganzzahlige Wert wird 1,0 zugeordnet, 0,0 ist 0.0 zugeordnet.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> multipliziert die resultierenden Gleitkommafarbwerte mit GL_c_SCALE und fügt sie GL_c_BIAS hinzu, wobei <em>c</em> für die jeweiligen Farbkomponenten ROT, GRÜN, BLAU und ALPHA ist. Die Ergebnisse werden an den Bereich [0,1] klammern.</li>
<li>Wenn GL_MAP_COLOR true ist, skaliert <strong>glDrawPixels</strong> jede Farbkomponente um die Größe der Nachschlagetabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw. A.</li>
<li>Die <strong>glDrawPixels-Funktion</strong> konvertiert die resultierenden RGBA-Farben in Fragmente, indem sie die aktuelle Rasterposition <em>z</em>-koordinate und Texturkoordinaten an jedes Pixel anfügen und dann <em>x-</em> und y-Fensterkoordinaten dem <em>n-th-Fragment</em>so zuweisen, <em>dass x</em>? <em></em> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> + <em>n /width</em><br/> Wobei (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist.<br/></li>
<li>Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Die <strong>glDrawPixels-Funktion</strong> wendet Texturzuordnungs-, Textur- und alle Fragmentvorgänge an, bevor die Fragmente in den Framepuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert diese Komponente in das interne Gleitkommaformat auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Grün und Blau auf 0,0 und Alpha auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert diese Komponente in das interne Gleitkommaformat auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot und Blau auf 0,0 und Alpha auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert diese Komponente in das interne Gleitkommaformat auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot und Grün auf 0,0 und Alpha auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alphakomponente.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert diese Komponente in das interne Gleitkommaformat auf die gleiche Weise wie die Alphakomponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot, Grün und Blau auf 0,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: Rot, Grün, Blau. Die <strong>glDrawPixels-Funktion</strong> konvertiert jede Komponente auf die gleiche Weise in das interne Gleitkommaformat wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Dreierfarbe wird in ein RGBA-Pixel konvertiert, wobei alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Leuchtdichtekomponente.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert diese Komponente in das interne Gleitkommaformat auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf den konvertierten Leuchtwert und alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von zwei Komponenten in dieser Reihenfolge: Leuchtdichte, Alpha.<br/> Die <strong>glDrawPixels-Funktion</strong> konvertiert die beiden Komponenten in das interne Gleitkommaformat auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf den konvertierten Leuchtwert und alpha auf den konvertierten Alphawert festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL_BGR_EXT stellt ein Format bereit, das dem Speicherlayout von Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br/> GL_BGRA_EXT stellt ein Format bereit, das dem Speicherlayout von Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *Pixel.* Im Folgenden sind die akzeptierten symbolischen Konstanten und ihre Bedeutungen.



| Wert                                                                                                                                                                      | Bedeutung                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | 8-Bit-Ganzzahl ohne Vorzeichen<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Ganze 8-Bit-Zahl mit Vorzeichen<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**GL \_ BITMAP**</dt> </dl>                          | Einzelne Bits in 8-Bit-Ganzzahlen ohne Vorzeichen<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | 16-Bit-Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Ganze 16-Bit-Zahl mit Vorzeichen<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | 32-Bit Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | 32-bit integer<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Gleitkomma mit einfacher Genauigkeit<br/>        |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Ein Zeiger auf die Pixeldaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                                                                          |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Entweder *format* oder *type* war kein akzeptierter Wert. <br/>                                                                                                                             |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Format:* GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE oder GL \_ LUMINANCE \_ ALPHA, und OpenGL befand sich im Farbindexmodus.<br/> |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Der Typ* war GL \_ BITMAP, und *das Format* war weder GL COLOR INDEX noch \_ GL \_ \_ STENCIL \_ INDEX.<br/>                                                                                         |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Format* war GL \_ STENCIL \_ INDEX, und es gab keinen Schablonenpuffer.<br/>                                                                                                                  |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                        |


## <a name="remarks"></a>Hinweise

Die **glDrawPixels-Funktion** liest Pixeldaten aus dem Arbeitsspeicher und schreibt sie relativ zur aktuellen Rasterposition in den Framepuffer. Verwenden Sie [**glRasterPos,**](glrasterpos-functions.md) um die aktuelle Rasterposition festzulegen, und verwenden [**Sie glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ CURRENT RASTER \_ \_ POSITION, um die Rasterposition abzufragen.

Mehrere Parameter definieren die Codierung von Pixeldaten im Arbeitsspeicher und steuern die Verarbeitung der Pixeldaten, bevor sie im Framepuffer platziert werden. Diese Parameter werden mit vier Funktionen festgelegt: [**glPixelStore,**](glpixelstore-functions.md) [**glPixelTransfer,**](glpixeltransfer.md) [**glPixelMap**](glpixelmap.md)und [**glPixelZoom.**](glpixelzoom.md) In diesem Thema werden die Auswirkungen vieler, aber nicht aller Parameter, die von diesen vier Funktionen angegeben werden, auf **glDrawPixels** beschrieben.

Daten werden aus *Pixeln* als Sequenz von Bytes mit oder ohne Vorzeichen, Shorts mit vorzeichen oder ohne Vorzeichen, ganze Zahlen mit oder ohne Vorzeichen oder Gleitkommawerte mit einfacher Genauigkeit gelesen, je nach *Typ*. Jedes dieser Bytes, Shorts, ganzen Zahlen oder Gleitkommawerte wird je nach *Format* als eine Farb- oder Tiefenkomponente oder als ein Index interpretiert. Indizes werden immer einzeln behandelt. Farbkomponenten werden wiederum basierend auf dem *Format* als Gruppen von einem, zwei, drei oder vier Werten behandelt. Sowohl einzelne Indizes als auch Gruppen von Komponenten werden als Pixel bezeichnet. Wenn *der Typ* GL BITMAP \_ ist, müssen die Daten nicht signierte Bytes sein, und das *Format* muss entweder GL COLOR INDEX oder \_ GL \_ \_ STENCIL \_ INDEX sein. Jedes Byte ohne Vorzeichen wird als acht 1-Bit-Pixel behandelt, wobei die Bitreihenfolge durch GL UNPACK LSB FIRST bestimmt wird \_ \_ \_ (siehe [**glPixelStore**](glpixelstore-functions.md)).

Die *Breite* nach *Höhe* Pixel werden aus dem Arbeitsspeicher gelesen, beginnend bei Position *Pixel*. Standardmäßig werden diese Pixel von benachbarten Speicherspeicherorten übernommen, mit der Ausnahme, dass der Lesezeiger nach dem Lesen aller *Pixelbreite* auf die nächste 4-Byte-Grenze erweitert wird. Die **glPixelStore-Funktion** gibt die 4-Byte-Zeilenausrichtung mit dem Argument GL \_ UNPACK \_ ALIGNMENT an. Sie können sie auf 1, 2, 4 oder 8 Bytes festlegen. Andere Pixelspeicherparameter geben unterschiedliche Lesezeigerverbesserungen an, sowohl vor dem Lesen des ersten Pixels als auch nach dem Lesen aller *Pixel der Breite.* Die **glPixelStore-Funktion** arbeitet auf grundlage der Werte mehrerer Parameter, die von [**glPixelTransfer und glPixelMap**](glpixeltransfer.md) angegeben werden, auf die einzelnen Pixel der Breite nach *Höhe,* die sie aus dem Arbeitsspeicher liest. [](glpixelmap.md) Die Details dieser Vorgänge sowie der Zielpuffer, in den die Pixel gezeichnet werden, sind spezifisch für das Format der Pixel, wie im *Format* angegeben.

Bei der bisher beschriebenen Rasterung wird ein Pixelzoomfaktor von 1,0 angenommen. Wenn Sie [**glPixelZoom**](glpixelzoom.md) verwenden, um die Zoomfaktoren *"x"* und *"y* Pixel" zu ändern, werden Pixel wie folgt in Fragmente konvertiert. Wenn (*xr,yr*) die aktuelle Rasterposition ist und sich ein bestimmtes Pixel in der *n-ten* Spalte und in der *m-ten* Zeile des Pixelrechtecks befindet, werden Fragmente für Pixel generiert, deren Mittelpunkte sich im Rechteck mit Ecken an befinden.

(*x*<sub>r</sub>  +  *zoom*? *n*, *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *zoom*? (*n* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*m* + 1))

where *zoom*? ist der Wert von GL \_ ZOOM \_ X, und *zoom*<sub>y</sub> ist der Wert von GL \_ ZOOM \_ Y.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glDrawPixels ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ POSITION

**glGet** mit argument GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





