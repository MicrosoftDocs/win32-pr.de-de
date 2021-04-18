---
title: glgetcolortableext-Funktion (GL. h)
description: Die glgetcolortableext-Funktion Ruft die Farbtabellen Daten der aktuellen Ziel Texturpalette ab.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glgetcolortableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343894"
---
# <a name="glgetcolortableext-function"></a>glgetcolortableext-Funktion

Die **glgetcolortableext** -Funktion Ruft die Farbtabellen Daten der aktuellen Ziel Texturpalette ab.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Ziel Textur, deren Palette geändert werden soll. Muss Textur \_ 1D oder Textur \_ 2D sein.

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
<li>Die Funktion " <strong>glgetcolortableext</strong> " konvertiert Gleit Komma Werte direkt in ein internes Format mit einer nicht spezifizierten Genauigkeit. Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare ganzzahlige Wert-1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</li>
<li>Die Funktion " <strong>glgetcolortableext</strong> " multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist. Die Ergebnisse werden an den Bereich [0, 1] gebunden.</li>
<li>Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glgetcolortableext</strong> jede Farbkomponente anhand der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</li>
<li>Die Funktion " <strong>glgetcolortableext</strong> " konvertiert die resultierenden RGBA-Farben in Fragmente, indem die aktuelle Raster Position z-Koordinate und die Texturkoordinaten an jedes Pixel angefügt werden und dann dem <em>n</em>-ten Fragment, z. b. <em>x</em>, <em>x</em> -und <em>y</em> -Fenster Koordinaten zugewiesen werden? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em>j</em>? = <em>y</em><sub>r</sub> + <em>n/Breite</em><br/> Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Die <strong>glgetcolortableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die rote Komponente eines RGBA-Pixels, konvertiert Sie dann in ein RGBA-Pixel, wobei Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem "Red" und "Blue" auf "0,0" und "Alpha" auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die blaue Komponente eines RGBA-Pixels und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot" und "grün" auf "0,0" und "Alpha" auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alpha Komponente.<br/> Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.<br/> Die Funktion " <strong>glgetcolortableext</strong> " konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Microsoft Windows-geräteunabhängigen Bitmaps (Disb) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.<br/></td>
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

Der Datentyp für *Daten*. Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.



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

Zeigt auf den Speicherort, an dem die zurückgegebenen Farbtabellen Informationen gespeichert werden sollen. Jeder Farbtabellen Eintrag wird so gespeichert, als ob es sich um ein einzelnes Pixel einer 1-D-Textur handelt. Da alle Texturen über eine Standardpalette verfügen, gibt **glgetcolortableext** immer Paletteninformationen zurück, auch wenn die Textur Daten nicht in einem Palettenformat vorliegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.<br/>                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetcolortableext** " Ruft die tatsächlichen Farbtabellen Daten ab, die von [**glcolortableext**](glcolortableext.md) und [**glcolorsubtableext**](glcolorsubtableext.md)angegeben werden.

Bei der **glgetcolortableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ . Um zu überprüfen, ob die Implementierung von OpenGL **glgetcolortableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions). Wenn Sie die Struktur von GL ext in der Struktur zurückgibt \_ \_ \_ , wird **glgetcolortableext** unterstützt. Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glcolorsubtableext**](glcolorsubtableext.md)
</dt> <dt>

[**glcolortableext**](glcolortableext.md)
</dt> <dt>

[**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glgetcolortableparameterivext**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





