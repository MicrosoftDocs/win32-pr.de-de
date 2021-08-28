---
title: glCopyPixels-Funktion (Gl.h)
description: Die glCopyPixels-Funktion kopiert Pixel in den Framepuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels-Funktion OpenGL
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
ms.openlocfilehash: 43c399b4ce63f84c41bcb2d65140356ac20a6ddd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479446"
---
# <a name="glcopypixels-function"></a>glCopyPixels-Funktion

Die **glCopyPixels-Funktion** kopiert Pixel in den Framepuffer.

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

Die x-Ebenenkoordinate des Fensters der unteren linken Ecke des rechteckigen Bereichs der zu kopierenden Pixel.

</dd> <dt>

*y* 
</dt> <dd>

Die Fensterkoordinate der linken unteren Ecke des rechteckigen Bereichs der zu kopierenden Pixel.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des rechteckigen Bereichs von Pixeln, die kopiert werden sollen. Darf nicht negativ sein.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhendimension des rechteckigen Bereichs von Pixeln, die kopiert werden sollen. Darf nicht negativ sein.

</dd> <dt>

*type* 
</dt> <dd>

Gibt an, ob **glCopyPixels** Farbwerte, Tiefenwerte oder Schablonenwerte kopieren soll. Die zulässigen symbolischen Konstanten sind .




| Wert | Bedeutung | 
|-------|---------|
| <span id="GL_COLOR"></span><span id="gl_color"></span><dl><dt><strong>GL_COLOR</strong></dt></dl> | Die <strong>glCopyPixels-Funktion</strong> liest Indizes oder RGBA-Farben aus dem Puffer, der derzeit als Lesequellpuffer angegeben ist (siehe <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br /> Wenn Sich OpenGL im Farbindexmodus befindet:<br /><ol><li>Jeder Index, der aus diesem Puffer gelesen wird, wird in ein Festkommaformat mit einer nicht angegebenen Anzahl von Bits rechts vom Binärpunkt konvertiert.</li><li>Jeder Index wird um GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt. Wenn GL_INDEX_SHIFT negativ ist, erfolgt die Verschiebung nach rechts. In beiden Fällen füllen null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.<br /></li><li>Wenn GL_MAP_COLOR true ist, wird der Index durch den Wert ersetzt, auf den er in der GL_PIXEL_MAP_I_TO_I der Nachschlagetabelle verweist.</li><li>Unabhängig davon, ob die Nachschlageersetzung des Indexes erfolgt oder nicht, wird der ganzzahlige Teil des Indexes <strong>mit</strong>2<em><sup>b</sup></em> 1 ed, wobei <em>b</em> die Anzahl der Bits in einem Farbindexpuffer ist.</li></ol>Wenn Sich OpenGL im RGBA-Modus befindet:<br /><ol><li>Die Rot-, Grün-, Blau- und Alphakomponenten jedes gelesenen Pixels werden in ein internes Gleitkommaformat mit nicht angegebener Genauigkeit konvertiert.</li><li>Die Konvertierung ordnet den größten darstellbaren Komponentenwert 1,0 und den Komponentenwert 0,0 zu.</li><li>Die resultierenden Gleitkommafarbwerte werden dann mit GL_c_SCALE multipliziert und GL_c_BIAS hinzugefügt, wobei <em>c</em> für die jeweiligen Farbkomponenten ROT, GRÜN, BLAU und ALPHA ist.</li><li>Die Ergebnisse werden an den Bereich [0,1] klammern.</li><li>Wenn GL_MAP_COLOR true ist, wird jede Farbkomponente anhand der Größe der GL_PIXEL_MAP_c_TO_c Nachschlagetabelle skaliert und dann durch den Wert ersetzt, auf den sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw. A. Die resultierenden Indizes oder RGBA-Farben werden dann in Fragmente konvertiert, indem die aktuelle Rasterposition <em>z</em>-coordinate und Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fensterkoordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ) zugewiesen,  +  <em></em>wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist und das Pixel das Pixel in der <em>i-Position</em> in der <em>j-Zeile</em> ist. Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Texturzuordnung, Oberfläche und alle Fragmentvorgänge werden angewendet, bevor die Fragmente in den Framepuffer geschrieben werden.<br /></li></ol> | 
| <span id="GL_DEPTH"></span><span id="gl_depth"></span><dl><dt><strong>GL_DEPTH</strong></dt></dl> | Tiefenwerte werden aus dem Tiefenpuffer gelesen und direkt in ein internes Gleitkommaformat mit nicht angegebener Genauigkeit konvertiert. Der resultierende Gleitkommatiefewert wird dann mit GL_DEPTH_SCALE multipliziert und GL_DEPTH_BIAS hinzugefügt. Das Ergebnis wird an den Bereich [0,1] klammern. <br /> Die resultierenden Tiefenkomponenten werden dann in Fragmente konvertiert, indem die aktuelle Rasterpositionsfarbe oder der Farbindex und die Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fensterkoordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub>j ) zugewiesen, wobei (  +  <em></em><em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist und das Pixel das Pixel in der <em>i-Position</em> in der <em>j-Zeile</em> ist. Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Texturzuordnung, Oberfläche und alle Fragmentvorgänge werden angewendet, bevor die Fragmente in den Framepuffer geschrieben werden.<br /> | 
| <span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl><dt><strong>GL_STENCIL</strong></dt></dl> | Schablonenindizes werden aus dem Schablonenpuffer gelesen und in ein internes Festkommaformat mit einer nicht angegebenen Anzahl von Bits rechts vom Binärpunkt konvertiert. Jeder Festkommaindex wird dann um GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt. Wenn GL_INDEX_SHIFT negativ ist, erfolgt die Verschiebung nach rechts. In beiden Fällen füllen null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus. Wenn GL_MAP_STENCIL true ist, wird der Index durch den Wert ersetzt, auf den er in der GL_PIXEL_MAP_S_TO_S der Nachschlagetabelle verweist. Unabhängig davon, ob die Nachschlageersetzung des Indexes erfolgt oder nicht, wird der ganzzahlige Teil des <strong>Indexes</strong>mit 2<sup>b</sup> bis 1 ed, wobei <em>b</em> die Anzahl der Bits im Schablonenpuffer ist. Die resultierenden Schablonenindizes werden dann in den Schablonenpuffer geschrieben, sodass der index read from the <em>i</em> location of the <em>j</em> row to location<em>(x</em><sub>r</sub>  +  <em>i</em>, <em>y</em><sub>r</sub>  +  <em>j</em>), wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist. Nur der Pixelbesitztest, der Scissor-Test und die Schablonenschreibmaske wirken sich auf diese Schreibvorgänge aus.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Die *Breite* oder Höhe war negativ.<br/>                                                                                     |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Der Typ* war GL \_ DEPTH, und es gab keinen Tiefenpuffer.<br/>                                                                        |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | *Type* war GL \_ STENCIL, und es gab keinen Schablonenpuffer.<br/>                                                                    |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glCopyPixels-Funktion** kopiert ein am Bildschirm ausgerichtetes Rechteck von Pixeln von der angegebenen Framepufferposition in einen Bereich relativ zur aktuellen Rasterposition. Der Vorgang ist nur gut definiert, wenn sich der gesamte Pixelquellbereich innerhalb des verfügbar gemachten Teils des Fensters befindet. Die Ergebnisse von Kopien von außerhalb des Fensters oder aus Bereichen des Fensters, die nicht verfügbar gemacht werden, sind hardwareabhängig und nicht definiert.

Die Parameter *x* und *y* geben die Fensterkoordinaten der unteren linken Ecke des rechteckigen Bereichs an, der kopiert werden soll. Die *Parameter für Breite* und *Höhe* geben die Abmessungen des rechteckigen Bereichs an, der kopiert werden soll. Sowohl *Breite* als auch *Höhe* müssen nicht negative Zeichen sein.

Mehrere Parameter steuern die Verarbeitung der Pixeldaten, während sie kopiert werden. Diese Parameter werden mit drei Funktionen festgelegt: [**glPixelTransfer,**](glpixeltransfer.md) [**glPixelMap**](glpixelmap.md)und [**glPixelZoom.**](glpixelzoom.md) In diesem Thema werden die Auswirkungen der meisten, aber nicht aller Parameter, die von diesen drei Funktionen angegeben werden, auf **glCopyPixels** beschrieben.

Die **glCopyPixels-Funktion** kopiert Werte aus jedem Pixel mit der unteren linken Ecke an (*x*  +  *i*, *y*  +  *j*) für 0 = *i*  <  *Breite* und 0 = *j*  <  *Höhe*. Dieses Pixel wird als *das i-Pixel* in der *j-Zeile* bezeichnet. Pixel werden in Zeilenreihenfolge von der untersten in die höchste Zeile kopiert, von links nach rechts in jeder Zeile.

Der *Typparameter* gibt an, ob Farb-, Tiefen- oder Schablonendaten kopiert werden sollen.

Bei der bisher beschriebenen Rasterung wird ein Pixelzoomfaktor von 1,0 angenommen. Wenn Sie [**glPixelZoom**](glpixelzoom.md) verwenden, um die Zoomfaktoren *"x"* und *"y* Pixel" zu ändern, werden Pixel wie folgt in Fragmente konvertiert. Wenn (*x*<sub>r</sub> , *y*<sub>r</sub> ) die aktuelle Rasterposition ist und sich ein bestimmtes Pixel an der *i-Position* in der *j-Zeile* des Quellpixelrechtecks befindet, werden Fragmente für Pixel generiert, deren Mittelpunkte sich im Rechteck mit Ecken an befinden.

(*x*<sub>r</sub>  +  *zoom*? i, y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*)

und

(*x*<sub>r</sub>  +  *zoom*? (*i* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1))

where *zoom*? ist der Wert von GL \_ ZOOM \_ X, und *zoom*<sub>y</sub> ist der Wert von GL \_ ZOOM \_ Y.

Von [**glPixelStore**](glpixelstore-functions.md) angegebene Modi haben keine Auswirkungen auf den Vorgang von **glCopyPixels**.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyPixels ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ RASTER \_ POSITION

**glGet** mit argument GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

Verwenden Sie , um das Farbpixel in der unteren linken Ecke des Fensters an die aktuelle Rasterposition zu kopieren.

**glCopyPixels**( 0, 0, 1, 1, GL \_ COLOR );

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





