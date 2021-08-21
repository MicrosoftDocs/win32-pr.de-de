---
title: glColorSubTableEXT-Funktion (Gl.h)
description: Die glColorSubTableEXT-Funktion gibt einen Teil der Palette der Zieltextur an, der ersetzt werden soll.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT-Funktion OpenGL
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
ms.openlocfilehash: 3d99b8dcef2ef21b4d75eb5262d2e3ecffa3804fa8e7a4889ae5dcbf8d68f018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081680"
---
# <a name="glcolorsubtableext-function"></a>glColorSubTableEXT-Funktion

Die **glColorSubTableEXT-Funktion** gibt einen Teil der Palette der Zieltextur an, der ersetzt werden soll.

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

Die Zielpalettentextur, deren Palette geändert werden soll. Muss TEXTURE \_ 1D oder TEXTURE \_ 2D sein.

</dd> <dt>

*start* 
</dt> <dd>

Der Indexeintrag der Anfangspalette der zu ändernden Palette.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der Palettenindexeinträge der Palette, die ab dem Start geändert *werden sollen.* Der *count-Parameter* bestimmt den Bereich der Palettenindexeinträge, die geändert werden.

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
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in der folgenden Reihenfolge: Rot, Grün, Blau, Alpha. Das RGBA-Format wird auf diese Weise bestimmt: <br/>
<ol>
<li>Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert Gleitkommawerte direkt in ein internes Format mit nicht angegebener Genauigkeit. Ganzzahlwerte mit Vorzeichen werden linear dem internen Format zugeordnet, damit der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: Der größte ganzzahlige Wert wird 1,0 zugeordnet, 0,0 ist 0.0 zugeordnet.</li>
<li>Die <strong>glColorSubTableEXT-Funktion</strong> multipliziert die resultierenden Farbwerte mit GL_c_SCALE und fügt sie GL_c_BIAS hinzu, wobei <em>c</em> für die jeweiligen Farbkomponenten ROT, GRÜN, BLAU und ALPHA ist. Die Ergebnisse werden an den Bereich [0,1] klammern.</li>
<li>Wenn GL_MAP_COLOR <strong>TRUE</strong>ist, skaliert <strong>glColorSubTableEXT</strong> jede Farbkomponente um die Größe der Nachschlagetabelle GL_PIXEL_MAP_c_TO_c und ersetzt die Komponente durch den Wert, auf den sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw. A.</li>
<li>Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert die resultierenden RGBA-Farben in Fragmente, indem sie die aktuelle Rasterposition <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel anfügen und dann <em>x-</em> und y-Fensterkoordinaten dem <em>n-th-Fragment</em>so zuweisen,<em>dass x</em>? <em></em> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em><br/> <em>y</em>? = <em>y</em><sub>r</sub> +<em>n/width</em><br/> Wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist.<br/></li>
<li>Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Die <strong>glColorSubTableEXT-Funktion</strong> wendet Texturzuordnungs-, Farb- und alle Fragmentvorgänge an, bevor die Fragmente in den Framepuffer geschrieben werden.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne rote Komponente.<br/> Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die rote Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem grün und blau auf 0,0 und alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne grüne Komponente.<br/> Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert diese Komponente in das interne Format auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot und Blau auf 0,0 und Alpha auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne blaue Komponente.<br/> Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die blaue Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot und Grün auf 0,0 und Alpha auf 1,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Jedes Pixel ist eine einzelne Alphakomponente.<br/> Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die Alphakomponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, bei dem Rot, Grün und Blau auf 0,0 festgelegt sind. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: Rot, Grün, Blau.<br/> Die <strong>glColorSubTableEXT-Funktion</strong> konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Dreifachfarbe wird in ein RGBA-Pixel konvertiert, bei dem alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br/> GL_BGR_EXT stellt ein Format zur Verfügung, das dem Speicherlayout Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows und OpenGL-Pixelfunktionsaufrufen verwenden.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br/> GL_BGRA_EXT stellt ein Format zur Verfügung, das dem Speicherlayout Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen dieselben Daten mit Windows und OpenGL-Pixelfunktionsaufrufen verwenden.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *die Daten*. Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT und GL \_ FLOAT.

In der folgenden Tabelle wird die Bedeutung der gültigen Konstanten für den *Typparameter* zusammengefasst.



| Wert                                                                                                                                                                      | Bedeutung                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | 8-Bit-Ganzzahl ohne Vorzeichen<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Ganze 8-Bit-Zahl mit Vorzeichen<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | 16-Bit-Ganzzahl ohne Vorzeichen<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Ganze 16-Bit-Zahl mit Vorzeichen<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | 32-Bit Ganzzahl ohne Vorzeichen<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | 32-bit integer<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Gleitkommawert mit einfacher Genauigkeit<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Ein Zeiger auf die Palettentexturdaten. Die Daten werden als einzelne Pixel eines 1D-Texturpaletteneintrags für einen Paletteneintrag behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                              | Bedeutung                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | *start* oder *count* war eine ungültige ganze Zahl.<br/>                                                                                 |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *target,* *format* oder *type* war kein akzeptierter Wert.<br/>                                                                    |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glColorSubTableEXT-Funktion** gibt Teile der Palette der aktuellen Zieltextur an, die ersetzt werden sollen. Im Gegensatz zu [**glColorTableEXT**](glcolortableext.md)können Sie den *Zielparameter* nicht als Proxytexturpalette angeben.

> [!Note]  
> Die **glColorSubTableEXT-Funktion** ist eine Erweiterungsfunktion, die nicht Teil der OpenGL-Standardbibliothek ist, sondern Teil der TEXTURerweiterung der GL \_ \_ \_ EXT-Palette ist. Um zu überprüfen, ob Ihre Implementierung von OpenGL **glColorSubTableEXT** unterstützt, rufen Sie [**glGetString**](glgetstring.md)(GL \_ EXTENSIONS) auf. Wenn die TEXTUR der GL \_ \_ EXT-Palette zurückgegeben \_ wird, wird **glColorSubTableEXT** unterstützt. Rufen Sie [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf, um die Funktionsadresse einer Erweiterungsfunktion abzurufen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





