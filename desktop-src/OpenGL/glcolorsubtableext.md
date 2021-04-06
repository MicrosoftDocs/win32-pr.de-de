---
title: glcolorsubtableext-Funktion (GL. h)
description: Die glcolorsubtableext-Funktion gibt einen Teil der zu ersetzenden Palette der Ziel Textur an.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glcolorsubtableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858981"
---
# <a name="glcolorsubtableext-function"></a>glcolorsubtableext-Funktion

Die **glcolorsubtableext** -Funktion gibt einen Teil der zu ersetzenden Palette der Ziel Textur an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zielstruktur, deren Palette geändert werden soll. Muss Textur \_ 1D oder Textur \_ 2D sein.

</dd> <dt>

*start* 
</dt> <dd>

Der Eintrag für die Start Palette der Palette, der geändert werden soll.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der Palettenindex Einträge der Palette, die beginnend beim *Start* geändert werden soll. Der *count* -Parameter bestimmt den Bereich der Palettenindex Einträge, die geändert werden.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden symbolischen Konstanten werden akzeptiert.



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
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in der folgenden Reihenfolge: rot, grün, blau, alpha. Das RGBA-Format wird auf diese Weise bestimmt: <br/>
<ol>
<li>Mit der <strong>glcolorsubtableext</strong> -Funktion werden Gleit Komma Werte direkt in ein internes Format mit nicht spezifizierter Genauigkeit konvertiert. Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 zugeordnet wird und der negativere darstellbare Wert-1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</li>
<li>Die <strong>glcolorsubtableext</strong> -Funktion multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist. Die Ergebnisse werden an den Bereich [0, 1] gebunden.</li>
<li>Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glcolorsubtableext</strong> jede Farbkomponente anhand der Größe der Such Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt die Komponente dann durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</li>
<li>Die <strong>glcolorsubtableext</strong> -Funktion konvertiert die resultierenden RGBA-Farben in Fragmente, indem die aktuelle Raster Position <em>z</em>-Koordinate und die Texturkoordinaten an jedes Pixel angefügt werden, und dann die <em>x</em> -und <em>y</em> -Fenster Koordinaten dem <em>n</em>-ten Fragment so<em>x</em>zugewiesen werden? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> +<em>n/Breite</em><br/> Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Die <strong>glcolorsubtableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die <strong>glcolorsubtableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die Funktion " <strong>glcolorsubtableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot" und "blau" auf "0,0" und "Alpha" auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die <strong>glcolorsubtableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alpha Komponente.<br/> Die Funktion " <strong>glcolorsubtableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.<br/> Die <strong>glcolorsubtableext</strong> -Funktion konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br/> GL_BGRA_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *Daten*. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.

In der folgenden Tabelle wird die Bedeutung der gültigen Konstanten für den *Typparameter* zusammengefasst.



| Wert                                                                                                                                                                      | Bedeutung                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL- \_ Byte ohne Vorzeichen \_**</dt> </dl>    | 8-Bit-Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ Byte**</dt> </dl>                                | Ganze 8-Bit-Zahl mit Vorzeichen<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ unsigned \_ Short**</dt> </dl> | 16-Bit-Ganzzahl ohne Vorzeichen<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ Short**</dt> </dl>                             | Ganze 16-Bit-Zahl mit Vorzeichen<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ unsigned \_ int**</dt> </dl>       | 32-Bit Ganzzahl ohne Vorzeichen<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | 32-bit integer<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | Gleitkommawert mit einfacher Genauigkeit<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die palettentextur Daten. Die Daten werden als einzelne Pixel eines 1-D-Textur paletteneintrags für einen Paletteneintrag behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | *Start* oder *count* war eine ungültige ganze Zahl.<br/>                                                                                 |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | *Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.<br/>                                                                    |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glcolorsubtableext** -Funktion gibt Teile der zu ersetzenden Palette der aktuellen Zieltextur an. Anders als bei [**glcolortableext**](glcolortableext.md)können Sie den *Ziel* Parameter nicht als Proxy Texturpalette angeben.

> [!Note]  
> Bei der **glcolorsubtableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ . Um zu überprüfen, ob die Implementierung von OpenGL **glcolorsubtableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions). Wenn Sie die Struktur "GL ext-Struktur" zurückgibt \_ \_ \_ , wird " **glcolorsubtableext** " unterstützt. Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolortableext**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetcolortableext**](glgetcolortableext.md)
</dt> <dt>

[**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glgetcolortableparameterivext**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





