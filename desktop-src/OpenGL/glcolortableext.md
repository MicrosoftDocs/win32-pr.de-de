---
title: glcolortableext-Funktion (GL. h)
description: Die glcolortableext-Funktion gibt das Format und die Größe einer Palette für die Zielstrukturen an.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glcolortableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742209"
---
# <a name="glcolortableext-function"></a>glcolortableext-Funktion

Die **glcolortableext** -Funktion gibt das Format und die Größe einer Palette für die Zielstrukturen an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Ziel Textur, deren Palette geändert werden soll. Muss Textur \_ 1D, Textur \_ 2D, Proxy \_ Textur \_ 1D oder Proxy \_ Textur \_ 2D sein.

</dd> <dt>

*internalformat* 
</dt> <dd>

Das interne Format und die Auflösung der Palette. Dieser Parameter kann einen der folgenden symbolischen Werte annehmen.



| Konstante       | Basis Format | R-Bits | G Bits | B Bits | Eine Bits |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ B2 | GL. \_ RGB     | 3      | 3      | 2      |        |
| GL \_ RGB4       | GL. \_ RGB     | 4      | 4      | 4      |        |
| GL \_ RGB5       | GL. \_ RGB     | 5      | 5      | 5      |        |
| GL \_ RGB8       | GL. \_ RGB     | 8      | 8      | 8      |        |
| GL \_ RGB10      | GL. \_ RGB     | 10     | 10     | 10     |        |
| GL \_ RGB12      | GL. \_ RGB     | 12     | 12     | 12     |        |
| GL \_ RGB16      | GL. \_ RGB     | 16     | 16     | 16     |        |
| GL \_ RGBA2      | GL \_ RGBA    | 2      | 2      | 2      | 2      |
| GL \_ RGBA4      | GL \_ RGBA    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ a1   | GL \_ RGBA    | 5      | 5      | 5      | 1      |
| GL \_ RGBA8      | GL \_ RGBA    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ a2   | GL \_ RGBA    | 10     | 10     | 10     | 2      |
| GL \_ RGB12      | GL \_ RGBA    | 12     | 12     | 12     | 12     |
| GL \_ RGBA16     | GL \_ RGBA    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* 
</dt> <dd>

Die Größe der Palette. Muss für eine Ganzzahl *n* 2 n = 1 sein.

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
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: rot, grün, blau, alpha. Das RGBA-Format wird auf diese Weise bestimmt: <br/>
<ol>
<li>Die <strong>glcolortableext</strong> -Funktion konvertiert Gleit Komma Werte direkt in ein internes Format mit einer nicht spezifizierten Genauigkeit. Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare ganzzahlige Wert-1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</li>
<li>Die Funktion " <strong>glcolortableext</strong> " multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist. Die Ergebnisse werden an den Bereich [0, 1] gebunden.</li>
<li>Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glcolortableext</strong> jede Farbkomponente anhand der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</li>
<li>Mit der <strong>glcolortableext</strong> -Funktion werden die resultierenden RGBA-Farben in Fragmente konvertiert, indem die aktuelle Raster Position <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden <em>x</em> -und <em>y</em> -Fenster Koordinaten für das <em>n</em>-te Fragment so<em>x</em>zugewiesen? = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em><br/> <em></em>Teenie? = <em>y</em><sub>r</sub> +<em>n/Breite</em><br/> Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.<br/></li>
<li>Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden. Die <strong>glcolortableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die rote Komponente eines RGBA-Pixels, konvertiert Sie dann in ein RGBA-Pixel, bei dem Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem "Red" und "Blue" auf "0,0" und "Alpha" auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die <strong>glcolortableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alpha Komponente.<br/> Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem rot, grün und blau auf 0,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.<br/> Die <strong>glcolortableext</strong> -Funktion konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
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



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Breite* war eine ungültige ganze Zahl.<br/>                                                                                            |
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | " *target*", " *internalformat*", " *Format*" oder " *Type* " war kein akzeptierter Wert.<br/>                                                 |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Palettentexturen werden mit einer Palette von Farben und einem Satz von Bilddaten definiert, die aus Indizes für Farbeinträge einer Palette (Farbtabelle) bestehen.

Die **glcolortableext** -Funktion gibt die Texturpalette einer Ziel Textur an. Er nimmt die *Daten* aus dem Arbeitsspeicher und konvertiert die Daten so, als ob jeder Paletteneintrag ein einzelnes Pixel einer 1-D-Textur ist. Die Funktion " **glcolortableext** " entpackt und konvertiert die Daten und übersetzt Sie in ein internes Format, das mit dem angegebenen *Format* so genau wie möglich übereinstimmt.

Wenn die *Breite* einer Palette größer ist als der Bereich der Farbindizes in den Textur Daten, werden einige der Paletteneinträge nicht verwendet. Wenn die *Breite* einer Palette kleiner ist als der Bereich der Farbindizes in den Textur Daten, werden die signifikantesten Bits der Textur Daten ignoriert, und nur die entsprechende Anzahl von Bits im Index wird beim Zugriff auf die Palette verwendet. Wenn Sie ein Proxy *Ziel* mithilfe der Proxy \_ Textur \_ 1D oder \_ der Proxy Textur \_ 2D angeben, wird die Größe der Palette der Proxy Textur geändert, und die Parameter werden festgelegt, aber es werden keine Daten übertragen oder darauf zugegriffen.

Wenn der *Ziel* Parameter GL- \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D ist, und die-Implementierung die für *Format* oder *Width* angegebenen Werte nicht unter  stützt, kann bei der Erstellung der angeforderten Farbtabelle ein Fehler auftreten. In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter haben den Wert 0 (null). Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellen Format und eine bestimmte Größe unterstützt, indem Sie **glcolortableext** mit einem Proxy Ziel aufrufen und dann [**glgetcolortableparameterivext**](glgetcolortableparameterivext.md) oder [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glcolortableext** festgelegten width-Parameter übereinstimmt. Wenn die abgerufene Breite 0 (null) ist, ist die Farbtabellen Anforderung von **glcolortable** fehlgeschlagen. Wenn die abgerufene Breite nicht NULL ist, können Sie **glcolortable** mit dem echten Ziel mit Textur \_ 1D oder Textur \_ 2D zum Festlegen der Farbtabelle abrufen.

> [!Note]  
> Bei der **glcolortableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ . Um zu überprüfen, ob die Implementierung von OpenGL **glcolortableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions). Wenn Sie die Struktur von GL ext in der Struktur zurückgibt \_ \_ \_ , wird **glcolortableext** unterstützt. Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.

 

Rufen Sie zum Abrufen der tatsächlichen Farbtabellen Daten, die durch die **glcolortableext** -Funktion angegeben werden, [**glgetcolortableext**](glgetcolortableext.md)auf. Um die Parameter (z. b. *Breite* und *Format*) der durch die Funktion " **glcolortableext** " angegebenen Farbtabelle abzurufen, rufen Sie die Funktion " **glgetcolortableparameterivext** " oder " **glgetcolortableparameterfvext** " auf.

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

[**glcolorsubtableext**](glcolorsubtableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetcolortableext**](glgetcolortableext.md)
</dt> <dt>

[**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glgetcolortableparameterivext**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





