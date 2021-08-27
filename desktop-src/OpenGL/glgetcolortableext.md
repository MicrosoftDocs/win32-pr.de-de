---
title: glGetColorTableEXT-Funktion (Gl.h)
description: Die glGetColorTableEXT-Funktion ruft die Farbtabellendaten der aktuellen Zieltexturpalette ab.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT-Funktion OpenGL
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
ms.openlocfilehash: 46593ac7b03781288d7d0d3932ced799dbbdfcff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469627"
---
# <a name="glgetcolortableext-function"></a>glGetColorTableEXT-Funktion

Die **glGetColorTableEXT-Funktion** ruft die Farbtabellendaten der aktuellen Zieltexturpalette ab.

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

Die Zieltextur, deren Palette geändert werden soll. Muss TEXTURE \_ 1D oder TEXTURE \_ 2D sein.

</dd> <dt>

*format* 
</dt> <dd>

Das Format der Pixeldaten. Die folgenden symbolischen Konstanten werden akzeptiert.




| Wert | Bedeutung | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Jedes Pixel ist eine Gruppe von vier Komponenten in der folgenden Reihenfolge: Rot, Grün, Blau, Alpha. Das RGBA-Format wird auf diese Weise bestimmt: <br /><ol><li>Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert Gleitkommawerte direkt in ein internes Format mit nicht angegebener Genauigkeit. Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare ganzzahlige Wert -1,0 zugeordnet wird. Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: Der größte ganzzahlige Wert wird 1,0 und 0,0 zugeordnet.</li><li>Die <strong>glGetColorTableEXT-Funktion</strong> multipliziert die resultierenden Farbwerte mit GL_c_SCALE und fügt sie GL_c_BIAS hinzu, wobei <em>c</em> für die jeweiligen Farbkomponenten ROT, GRÜN, BLAU und ALPHA ist. Die Ergebnisse werden an den Bereich [0,1] klammern.</li><li>Wenn GL_MAP_COLOR <strong>TRUE</strong>ist, skaliert <strong>glGetColorTableEXT</strong> jede Farbkomponente nach der Größe der Nachschlagetabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw. A.</li><li>Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert die resultierenden RGBA-Farben in Fragmente, indem sie die aktuelle Rasterposition z-Koordinate und Texturkoordinaten an jedes Pixel anfügt und dann dem <em>n-ten</em>Fragment <em>x-</em> und y-Fensterkoordinaten zuweist, sodass <em>x</em>? <em></em> = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Rasterposition ist.<br /></li><li>Diese Pixelfragmente werden dann genau wie die Fragmente behandelt, die durch Rastern von Punkten, Linien oder Polygonen generiert werden. Die <strong>glGetColorTableEXT-Funktion</strong> wendet Texturzuordnung, Oberfläche und alle Fragmentvorgänge an, bevor die Fragmente in den Framepuffer geschrieben werden.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Jedes Pixel ist eine einzelne rote Komponente.<br /> Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert diese Komponente in das interne Format auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels. Anschließend wird sie in ein RGBA-Pixel konvertiert, wobei grün und blau auf 0,0 und alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Jedes Pixel ist eine einzelne grüne Komponente.<br /> Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert diese Komponente in das interne Format auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, wobei rot und blau auf 0,0 und alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Jedes Pixel ist eine einzelne blaue Komponente.<br /> Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert diese Komponente in das interne Format auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Jedes Pixel ist eine einzelne Alphakomponente.<br /> Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert diese Komponente in das interne Format auf die gleiche Weise wie die Alphakomponente eines RGBA-Pixels und konvertiert sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.<br /> Die <strong>glGetColorTableEXT-Funktion</strong> konvertiert jede Komponente in das interne Format auf die gleiche Weise wie die roten, grünen und blauen Komponenten eines RGBA-Pixels. Die Dreierfarbe wird in ein RGBA-Pixel konvertiert, wobei alpha auf 1,0 festgelegt ist. Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.<br /> GL_BGR_EXT stellt ein Format bereit, das dem Speicherlayout von Microsoft Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.<br /> GL_BGRA_EXT stellt ein Format bereit, das dem Speicherlayout von Windows geräteunabhängigen Bitmaps (DIBs) entspricht. Daher können Ihre Anwendungen die gleichen Daten mit Windows Funktionsaufrufen und OpenGL-Pixelfunktionsaufrufen verwenden.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Der Datentyp für *die Daten.* Im Folgenden sind die akzeptierten symbolischen Konstanten und ihre Bedeutungen.



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

Zeigt auf den Speicherort, an dem die zurückgegebenen Farbtabelleninformationen gespeichert werden sollen. Jeder Farbtabelleneintrag wird so gespeichert, als wäre er ein einzelnes Pixel einer 1D-Textur. Da alle Texturen über eine Standardpalette verfügen, gibt **glGetColorTableEXT** immer Paletteninformationen zurück, auch wenn die Texturdaten nicht in einem Palettenformat vorliegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *Ziel,* *Format* oder *Typ* war kein akzeptierter Wert.<br/>                                                                   |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetColorTableEXT-Funktion** ruft die tatsächlichen Farbtabellendaten ab, die von [**glColorTableEXT**](glcolortableext.md) und [**glColorSubTableEXT**](glcolorsubtableext.md)angegeben werden.

Die **glGetColorTableEXT-Funktion** ist eine Erweiterungsfunktion, die nicht Teil der OpenGL-Standardbibliothek ist, sondern Teil der \_ GL \_ EXT-Palettentexturerweiterung \_ ist. Um zu überprüfen, ob Ihre OpenGL-Implementierung **glGetColorTableEXT** unterstützt, rufen Sie [**glGetString**](glgetstring.md)(GL \_ EXTENSIONS) auf. Wenn die Textur der GL \_ EXT-Palette zurückgegeben \_ \_ wird, wird **glGetColorTableEXT** unterstützt. Rufen Sie [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf, um die Funktionsadresse einer Erweiterungsfunktion abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





