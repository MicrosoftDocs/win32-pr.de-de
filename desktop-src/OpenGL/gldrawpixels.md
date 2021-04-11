---
title: gldrawpixels-Funktion (GL. h)
description: Die gldrawpixels-Funktion schreibt einen Block von Pixeln in den Framebuffer.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- gldrawpixels-Funktion OpenGL
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
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103199"
---
# <a name="gldrawpixels-function"></a>gldrawpixels-Funktion

Die **gldrawpixels** -Funktion schreibt einen Block von Pixeln in den Framebuffer.

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

Die Width-Dimension des Pixel Rechtecks, das in den Framebuffer geschrieben wird.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhen Dimension des Pixel Rechtecks, das in den Framebuffer geschrieben wird.

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
<li>Die <strong>gldrawpixels</strong> -Funktion konvertiert jedes Pixel in ein fest Komma Format, wobei eine nicht angegebene Anzahl von Bits auf der rechten Seite des binären Punkts ist, unabhängig vom Arbeitsspeicher Datentyp. Gleit Komma Werte werden in echte Werte für einen bestimmten Wert konvertiert. Die Funktion " <strong>gldrawpixels</strong> " konvertiert ganzzahlige Daten mit und ohne Vorzeichen mit allen Bruch Bits, die auf NULL festgelegt sind. Die-Funktion konvertiert Bitmapdaten in 0,0 oder 1,0.</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " verschiebt jeden Index des festpunkts nach links GL_INDEX_SHIFT Bits und fügt Sie GL_INDEX_OFFSET hinzu. Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite. In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</li>
<li>Im RGBA-Modus konvertiert <strong>gldrawpixels</strong> den resultierenden Index mithilfe der Tabellen GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B und GL_PIXEL_MAP_I_TO_A in ein RGBA-Pixel. Wenn im Farb Index Modus und GL_MAP_COLOR den Wert true hat, wird der Index durch den Wert ersetzt, auf den <strong>gldrawpixels</strong> in der Nachschlage Tabelle GL_PIXEL_MAP_I_TO_I verweist.</li>
<li>Unabhängig davon, ob die Such Ersetzung des Indexes <strong>abgeschlossen ist oder</strong>nicht, wird der ganzzahlige Teil des Indexes mit 2<sup>b</sup> - 1, d. <em>h</em> . die Anzahl der Bits in einem Farb Index Puffer, festgestellt.</li>
<li>Die resultierenden Indizes oder RGBA-Farben werden dann in Fragmente konvertiert, indem die aktuelle Raster Position <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel angefügt werden, und dann werden <em>x</em> -und <em>y</em> -Fenster Koordinaten dem <em>n</em>-ten Fragment wie <em>x</em>zugewiesen. = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> + <em>n/Breite</em><br/> Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Die <strong>gldrawpixels</strong> -Funktion behandelt diese Pixel Fragmente genau wie die Fragmente, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Es wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Jedes Pixel ist ein einzelner Wert, ein Schablone-Index. <br/>
<ol>
<li>Die Funktion " <strong>gldrawpixels</strong> " konvertiert sie in ein fest Komma Format, wobei eine nicht angegebene Anzahl von Bits auf der rechten Seite des binären Punkts ist, unabhängig vom Arbeitsspeicher Datentyp. Gleit Komma Werte werden in echte Werte für einen bestimmten Wert konvertiert. Die Funktion " <strong>gldrawpixels</strong> " konvertiert ganzzahlige Daten mit und ohne Vorzeichen mit allen Bruch Bits, die auf NULL festgelegt sind. Bitmapdaten werden entweder in 0,0 oder 1,0 konvertiert.</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " verschiebt jeden Index des festpunkts nach links GL_INDEX_SHIFT Bits und fügt Sie GL_INDEX_OFFSET hinzu. Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite. In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</li>
<li>Wenn GL_MAP_STENCIL true ist, wird der Index durch den Wert ersetzt, auf den <strong>gldrawpixels</strong> in der Nachschlage Tabelle GL_PIXEL_MAP_S_TO_S verweist.</li>
<li>Unabhängig davon, ob die Such Ersetzung des Indexes abgeschlossen ist oder nicht, wird der ganzzahlige Teil des Indexes dann mit 2<sup>b</sup> 1 <strong>und</strong>mit 2 b - 1, wobei <em>b</em> die Anzahl der Bits im Schablonen Puffer ist. Die resultierenden Schablone-Indizes werden dann in den Schablonen Puffer geschrieben, sodass der <em>n</em>-te Index in den Speicherort <em>x</em>geschrieben wird? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> + <em>n/Breite</em><br/> Where (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) ist die aktuelle Raster Position. Diese Schreibvorgänge wirken sich nur auf den Pixel Besitz Test, den Scheren Test und die Schablone-Schreibvorgängen aus.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Einzel Tiefe Komponente. <br/>
<ol>
<li>Die Funktion " <strong>gldrawpixels</strong> " konvertiert Gleit Komma Daten direkt in ein internes Gleit Komma Format mit nicht spezifizierter Genauigkeit. Ganzzahlige Daten mit Vorzeichen werden linear dem internen Gleit Komma Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " multipliziert den resultierenden Wert für Gleit Komma Tiefe GL_DEPTH_SCALE und fügt Sie GL_DEPTH_BIAS hinzu. Das Ergebnis wird an den Bereich [0, 1] gebunden.</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " konvertiert die resultierenden tiefen Komponenten in Fragmente, indem die aktuelle Raster Positions Farbe bzw. der Farb Index und die Texturkoordinaten an jedes Pixel angefügt werden und dann dem <em>n</em> -ten Fragment dieses <em>x</em> <em>x</em> -und <em>y</em> -Fenster Koordinaten zugewiesen werden? = <em></em>x<sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> + <em>n/Breite</em><br/> Where ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Die <strong>gldrawpixels</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe mit vier Komponenten in dieser Reihenfolge: rot, grün, blau, alpha. <br/>
<ol>
<li>Die Funktion " <strong>gldrawpixels</strong> " konvertiert Gleit Komma Werte direkt in ein internes Gleit Komma Format mit nicht spezifizierter Genauigkeit. Ganzzahlige Werte mit Vorzeichen werden linear dem internen Gleit Komma Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " multipliziert die resultierenden Gleit Komma Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist. Die Ergebnisse werden an den Bereich [0, 1] gebunden.</li>
<li>Wenn GL_MAP_COLOR auf true festgelegt ist, skaliert <strong>gldrawpixels</strong> jede Farbkomponente anhand der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</li>
<li>Die Funktion " <strong>gldrawpixels</strong> " konvertiert die resultierenden RGBA-Farben in Fragmente, indem die aktuelle Raster Position <em>z</em>-Koordinate und die Texturkoordinaten an jedes Pixel angefügt werden, und dann die <em>x</em> -und <em>y</em> -Fenster Koordinaten dem <em>n</em>-ten Fragment so <em>x</em>zugewiesen werden? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> + <em>n/Width</em><br/> Where (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Die <strong>gldrawpixels</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert diese Komponente auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, wobei Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot" und "blau" auf "0,0" und "Alpha" auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert diese Komponente auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alpha Komponente.<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau. Die Funktion " <strong>gldrawpixels</strong> " konvertiert jede Komponente auf die gleiche Weise wie die roten, grünen und blauen Komponenten eines RGBA-Pixels in das interne Gleit Komma Format. Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Leuchtkraft Komponente.<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert diese Komponente auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot", "grün" und "blau" auf den konvertierten Wert für "Leuchtkraft" und "Alpha" auf "1,0" festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von zwei Komponenten in dieser Reihenfolge: "Leuchtkraft", "Alpha".<br/> Die Funktion " <strong>gldrawpixels</strong> " konvertiert die beiden Komponenten auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels in das interne Gleit Komma Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem rot, grün und blau auf den konvertierten Wert für die Leuchtkraft festgelegt sind, und Alpha auf den konvertierten Alpha Wert festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br/> GL_BGRA_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *Pixel*. Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.



| Wert                                                                                                                                                                      | Bedeutung                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL- \_ Byte ohne Vorzeichen \_**</dt> </dl>    | 8-Bit-Ganzzahl ohne Vorzeichen<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ Byte**</dt> </dl>                                | Ganze 8-Bit-Zahl mit Vorzeichen<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**GL- \_ Bitmap**</dt> </dl>                          | Einzelne Bits in 8-Bit-Ganzzahlen ohne Vorzeichen<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ unsigned \_ Short**</dt> </dl> | 16-Bit-Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ Short**</dt> </dl>                             | Ganze 16-Bit-Zahl mit Vorzeichen<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ unsigned \_ int**</dt> </dl>       | 32-Bit Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | 32-bit integer<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Gleit Komma Wert mit einfacher Genauigkeit<br/>        |



 

</dd> <dt>

*Pixel* 
</dt> <dd>

Ein Zeiger auf die Pixeldaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                                                                          |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Entweder *Format* oder *Typ* war kein akzeptierter Wert. <br/>                                                                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Format* : GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ Alpha, und OpenGL war im Farb Index Modus.<br/> |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Typ* : GL \_ Bitmap und *Format* war weder der GL \_ - \_ Farbindex noch der GL- \_ Schablonen \_ Index.<br/>                                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Format* war der GL \_ \_ -Schablonen Index, und es gab keinen Schablonen Puffer.<br/>                                                                                                                  |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                                        |


## <a name="remarks"></a>Bemerkungen

Die **gldrawpixels** -Funktion liest Pixeldaten aus dem Arbeitsspeicher und schreibt sie relativ zur aktuellen Raster Position in den Frame Puffer. Verwenden Sie [**glRasterPos**](glrasterpos-functions.md) , um die aktuelle Raster Position festzulegen, und verwenden Sie [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit \_ der aktuellen Raster Position von Argument GL, \_ \_ um die Raster Position abzufragen.

Mehrere Parameter definieren die Codierung von Pixeldaten im Arbeitsspeicher und steuern die Verarbeitung der Pixeldaten, bevor Sie im Framebuffer abgelegt werden. Diese Parameter werden mit vier Funktionen festgelegt: [**glpixelstore**](glpixelstore-functions.md), [**glpixeltransfer**](glpixeltransfer.md), [**glpixelmap**](glpixelmap.md)und [**glpixelzoom**](glpixelzoom.md). In diesem Thema werden die Auswirkungen auf **gldrawpixels** von vielen, jedoch nicht allen Parametern beschrieben, die von diesen vier Funktionen angegeben werden.

Daten werden aus *Pixeln* als Sequenz von Zeichen mit oder ohne Vorzeichen, mit Vorzeichen oder ohne Vorzeichen, mit Vorzeichen mit Vorzeichen oder ohne Vorzeichen oder mithilfe von Gleit Komma Werten mit einfacher Genauigkeit, abhängig vom *Typ*, gelesen. Jede dieser bytes, Shorts, Integer oder Gleit Komma Werte wird als eine Farb-oder tiefen Komponente oder je nach *Format* als ein Index interpretiert. Indizes werden immer einzeln behandelt. Farbkomponenten werden als Gruppen von einem, zwei, drei oder vier Werten behandelt, das wiederum auf dem- *Format* basiert. Sowohl einzelne Indizes als auch Gruppen von Komponenten werden als Pixel bezeichnet. Wenn der *Typ* "GL \_ Bitmap" ist, müssen die Daten nicht signierte Bytes sein, und das *Format* muss entweder "GL \_ Color Index" oder " \_ GL \_ Stencil \_ Index" lauten. Jedes Byte ohne Vorzeichen wird als 8 1-Bit-Pixel behandelt, wobei die bitanordnung zuerst von GL \_ Entpack \_ lsb \_ ( [**Siehe glpixelstore**](glpixelstore-functions.md)) bestimmt wird.

Die *Breite* nach *Höhe* von Pixel wird aus dem Arbeitsspeicher gelesen, beginnend an Position *Pixel*. Standardmäßig werden diese Pixel aus angrenzenden Speicherorten entnommen, mit dem Unterschied, dass nach dem Lesen aller *Breite* Pixel der Lese Zeiger auf die nächste 4-Byte-Grenze erweitert wird. Die Funktion " **glpixelstore** " gibt die 4-Byte-Zeilen Ausrichtung mit dem Argument "GL \_ unpack \_ Alignment" an, und Sie können Sie auf 1, 2, 4 oder 8 Bytes festlegen. Mit anderen Pixel Speicher Parametern werden unterschiedliche Lese Zeiger Erweiterungen angegeben, sowohl vor dem Lesen des ersten Pixels als auch nach dem Lesen aller *Breite* Pixel. Die **glpixelstore** -Funktion wird auf der Grundlage der Werte von mehreren Parametern, die von [**glpixeltransfer**](glpixeltransfer.md) und [**glpixelmap**](glpixelmap.md)angegeben werden, auf die einzelnen Werte der *Breite und Höhe* angewendet, die aus dem Arbeitsspeicher gelesen werden. Die Details dieser Vorgänge und der Ziel Puffer, in den die Pixel gezeichnet werden, sind für das Format der Pixel spezifisch, wie durch das *Format* angegeben.

Die bisher beschriebene rasterisierung setzt die Pixel Zoomfaktoren von 1,0 voraus. Wenn Sie mit [**glpixelzoom**](glpixelzoom.md) die *x* -und *y* -Pixel Zoomfaktoren ändern, werden Pixel wie folgt in Fragmente konvertiert. Wenn (*XR, yr*) die aktuelle Raster Position ist und ein angegebenes Pixel in der *n*-ten und der *m*-ten Zeile des Pixel Rechtecks liegt, werden Fragmente für Pixel generiert, deren zentriert sich in dem Rechteck mit Ecken bei befindet.

(*x*<sub>r</sub>  +  *Zoom*? *n*, *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *Zoom*? (*n* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*m* + 1))

Where *Zoom*? der Wert von GL \_ Zoom \_ X und *Zoom*<sub>y</sub> ist der Wert von GL \_ Zoom \_ y.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **gldrawpixels** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position

**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig

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

[**glalphafunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glpixelmap**](glpixelmap.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glpixelzoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glscissor**](glscissor.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> </dl>

 

 





