---
title: glcopypixels-Funktion (GL. h)
description: Die Funktion "glcopypixels" kopiert Pixel im Framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glcopypixels-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956602"
---
# <a name="glcopypixels-function"></a>glcopypixels-Funktion

Die Funktion " **glcopypixels** " kopiert Pixel im Framebuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die x-Ebenen-Koordinate der unteren linken Ecke des rechteckigen Bereichs, der kopiert werden soll.

</dd> <dt>

*y* 
</dt> <dd>

Die y-ebenenkoordinate des Fensters der unteren linken Ecke des rechteckigen Bereichs von Pixeln, die kopiert werden sollen.

</dd> <dt>

*width* 
</dt> <dd>

Die Width-Dimension des rechteckigen Bereichs von Pixeln, der kopiert werden soll. Darf nicht negativ sein.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhen Dimension des rechteckigen Bereichs von Pixeln, die kopiert werden soll. Darf nicht negativ sein.

</dd> <dt>

*type* 
</dt> <dd>

Gibt an, ob **glcopypixels** Farbwerte, tiefen Werte oder Schablonen Werte kopieren soll. Die zulässigen symbolischen Konstanten sind.



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
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td>Die Funktion " <strong>glcopypixels</strong> " liest Indizes oder RGBA-Farben aus dem Puffer, der derzeit als Lese Quell Puffer angegeben ist (siehe <a href="glreadbuffer.md"><strong>gllesebuffer</strong></a>). <br/> Wenn sich OpenGL im Farb Index Modus befindet:<br/>
<ol>
<li>Jeder aus diesem Puffer gelesene Index wird in ein fest Komma Format mit einer nicht angegebenen Anzahl von Bits auf der rechten Seite des Binär Punkts konvertiert.</li>
<li>Jeder Index wird von GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt. Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite. In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.<br/></li>
<li>Wenn GL_MAP_COLOR true ist, wird der Index durch den Wert ersetzt, auf den in der Nachschlage Tabelle GL_PIXEL_MAP_I_TO_I verwiesen wird.</li>
<li>Unabhängig davon, ob die Such Ersetzung des Indexes abgeschlossen ist oder nicht, wird der ganzzahlige Teil des <strong></strong>Indexes dann mit 2<em><sup>b</sup></em> 1, wobei <em>b</em> die Anzahl der Bits in einem Farb Index Puffer ist.</li>
</ol>
Wenn sich OpenGL im RGBA-Modus befindet:<br/>
<ol>
<li>Die roten, grünen, blauen und Alpha Komponenten jedes gelesenen Pixels werden in ein internes Gleit Komma Format mit einer nicht spezifizierten Genauigkeit konvertiert.</li>
<li>Bei der Konvertierung wird der größte darstellbare Komponenten Wert 1,0 und der Komponenten Wert 0 bis 0,0 zugeordnet.</li>
<li>Die resultierenden Gleit Komma Farbwerte werden dann mit GL_c_SCALE multipliziert und GL_c_BIAS hinzugefügt, wobei <em>c</em> für die jeweiligen Farbkomponenten Rot, grün, blau und Alpha ist.</li>
<li>Die Ergebnisse werden an den Bereich [0, 1] gebunden.</li>
<li>Wenn GL_MAP_COLOR true ist, wird jede Farbkomponente von der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c skaliert und dann durch den Wert ersetzt, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw.. Die resultierenden Indizes oder RGBA-Farben werden dann in Fragmente konvertiert, indem die aktuelle Raster Position <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fenster Koordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>) zugewiesen, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position ist, und das Pixel ist das Pixel an der Position <em>i</em> in der <em>j</em> -Zeile. Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Textur Zuordnung, Nebel und alle fragmentvorgänge werden angewendet, bevor die Fragmente in den Framebuffer geschrieben werden.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>Tiefen Werte werden aus dem tiefen Puffer gelesen und direkt in ein internes Gleit Komma Format mit nicht spezifizierter Genauigkeit konvertiert. Der resultierende Gleit Komma tiefen Wert wird dann mit GL_DEPTH_SCALE multipliziert und GL_DEPTH_BIAS hinzugefügt. Das Ergebnis wird an den Bereich [0, 1] gebunden. <br/> Die resultierenden tiefen Komponenten werden dann in Fragmente konvertiert, indem die aktuelle Raster Positions Farbe oder der aktuelle Farb Index und die Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fenster Koordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>) zugewiesen, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position und das Pixel das Pixel an der Position <em>i</em> in der <em>j</em> -Zeile ist. Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Textur Zuordnung, Nebel und alle fragmentvorgänge werden angewendet, bevor die Fragmente in den Framebuffer geschrieben werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>Schablone-Indizes werden aus dem Schablonen Puffer gelesen und in ein internes fest Komma Format mit einer nicht angegebenen Anzahl von Bits auf der rechten Seite des binären Punkts konvertiert. Jeder Index des Index wird dann von GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt. Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite. In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus. Wenn GL_MAP_STENCIL true ist, wird der Index durch den Wert ersetzt, auf den in der Nachschlage Tabelle GL_PIXEL_MAP_S_TO_S verwiesen wird. Unabhängig davon, ob die Such Ersetzung des Indexes abgeschlossen ist oder nicht, wird der ganzzahlige Teil des Indexes dann mit 2<sup>b</sup> 1 <strong>und</strong>mit 2 b - 1, wobei <em>b</em> die Anzahl der Bits im Schablonen Puffer ist. Die resultierenden Schablonen Indizes werden dann in den Schablonen Puffer geschrieben, sodass der aus dem <em>i</em> -Speicherort der <em>j</em> -Zeile gelesene Index in den Speicherort (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>) geschrieben wird, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position ist. Diese Schreibvorgänge wirken sich nur auf den Pixel Besitz Test, den Scheren Test und die Schablone-Schreibvorgängen aus.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Typ* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Die *Breite* oder Höhe war negativ.<br/>                                                                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Type* war GL \_ -Tiefe, und es gab keinen tiefen Puffer.<br/>                                                                        |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | *Typ* : GL \_ -Schablone und kein Schablone-Puffer.<br/>                                                                    |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glcopypixels** " kopiert ein Bildschirm gerichtetes Rechteck aus Pixeln vom angegebenen Frame Puffer-Speicherort in einen Bereich relativ zur aktuellen Raster Position. Der Vorgang ist nur dann klar definiert, wenn sich der gesamte Pixel Quellbereich innerhalb des verfügbar gemachten Teils des Fensters befindet. Die Ergebnisse von Kopien von außerhalb des Fensters oder aus den nicht verfügbar gemachten Fenstern sind Hardware abhängig und nicht definiert.

Der *x* -und der *y* -Parameter geben die Fenster Koordinaten der unteren linken Ecke des rechteckigen Bereichs an, der kopiert werden soll. Die *Width* -und *height* -Parameter geben die Dimensionen des rechteckigen Bereichs an, der kopiert werden soll. Sowohl " *Width* " als auch " *height* " dürfen nicht negativ sein.

Mehrere Parameter steuern die Verarbeitung der Pixeldaten, während diese kopiert werden. Diese Parameter werden mit drei Funktionen festgelegt: [**glpixeltransfer**](glpixeltransfer.md), [**glpixelmap**](glpixelmap.md)und [**glpixelzoom**](glpixelzoom.md). In diesem Thema werden die Auswirkungen auf **glcopypixels** der meisten, aber nicht alle Parameter beschrieben, die von diesen drei Funktionen angegeben werden.

Die Funktion " **glcopypixels** " kopiert Werte von jedem Pixel mit der unteren linken Ecke um (*x*  +  *i*, *y*  +  *j*) für 0 = *i*  <  *Width* und 0 = *j*  <  *height*. Dieses Pixel ist das *i* -Pixel in der *j* -Zeile. Pixel werden in Zeilen Reihenfolge von der niedrigsten zur höchsten Zeile (von links nach rechts) in jeder Zeile kopiert.

Der *Typparameter* gibt an, ob Farbe, Tiefe oder Schablonen Daten kopiert werden sollen.

Die bisher beschriebene rasterisierung setzt die Pixel Zoomfaktoren von 1,0 voraus. Wenn Sie mit [**glpixelzoom**](glpixelzoom.md) die *x* -und *y* -Pixel Zoomfaktoren ändern, werden Pixel wie folgt in Fragmente konvertiert. Wenn (*x*<sub>r</sub> , *y*<sub>r</sub> ) die aktuelle Raster Position ist und sich ein angegebenes Pixel an der *i* -Position in der *j* -Zeile des Quell Pixel Rechtecks befindet, werden Fragmente für Pixel generiert, deren Mittelpunkt in dem Rechteck mit Ecken liegt.

(*x*<sub>r</sub>  +  *Zoom*? i, y <sub>r</sub>  +  *Zoom*<sub>y</sub> *j*)

und

(*x*<sub>r</sub>  +  *Zoom*? (*i* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))

Where *Zoom*? der Wert von GL \_ Zoom \_ X und *Zoom*<sub>y</sub> ist der Wert von GL \_ Zoom \_ y.

Von [**glpixelstore**](glpixelstore-functions.md) angegebene Modi haben keine Auswirkung auf den Vorgang von **glcopypixels**.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcopypixel** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position

**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig

Um das Farb Pixel in der unteren linken Ecke des Fensters an die aktuelle Raster Position zu kopieren, verwenden Sie

**glcopypixels**(0, 0, 1, 1, GL- \_ Farbe);

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

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glread Buffer**](glreadbuffer.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> </dl>

 

 





