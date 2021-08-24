---
title: glGetColorTableParameterivEXT-Funktion (Gl.h)
description: Die Funktionen glGetColorTableParameterfvEXT und glGetColorTableParameterivEXT erhalten Palettenparameter aus Farbtabellen. | glGetColorTableParameterivEXT-Funktion (Gl.h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glGetColorTableParameterivEXT-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc45217d420aab9c5db3b1ceb416c369b5fb948df2911ea20e6e174eeed0649f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742032"
---
# <a name="glgetcolortableparameterivext-function"></a>glGetColorTableParameterivEXT-Funktion

Die Funktionen [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) und **glGetColorTableParameterivEXT** erhalten Palettenparameter aus Farbtabellen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur der Palette, für die Parameterdaten verwendet werden sollen. Muss TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D oder PROXY \_ TEXTURE \_ 2D sein.

</dd> <dt>

*pname* 
</dt> <dd>

Eine symbolische Konstante für den Typ der Palettenparameterdaten, auf die *params* zeigt.

Im Folgenden sind die akzeptierten symbolischen Konstanten und ihre Bedeutungen.



| Wert                                                                                                                                                                                                             | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ FORMAT \_ EXT**</dt> </dl>              | Gibt das interne Format zurück, das durch den letzten Aufruf von [**glColorTableEXT**](glcolortableext.md) oder den Standardwert angegeben wird.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ WIDTH \_ EXT**</dt> </dl>                 | Gibt die Breite der aktuellen Palette zurück.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ RED \_ SIZE \_ EXT**</dt> </dl>       | Gibt die tatsächliche Größe zurück, die intern zum Speichern der roten Komponente der Palettendaten verwendet wird.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ GREEN \_ SIZE \_ EXT**</dt> </dl> | Gibt die tatsächliche Größe zurück, die intern zum Speichern der grünen Komponente der Palettendaten verwendet wird.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ BLUE \_ SIZE \_ EXT**</dt> </dl>    | Gibt die tatsächliche Größe zurück, die intern zum Speichern der blauen Komponente der Palettendaten verwendet wird.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ ALPHA \_ SIZE \_ EXT**</dt> </dl> | Gibt die tatsächliche Größe zurück, die intern zum Speichern der Alphakomponente der Palettendaten verwendet wird.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Zeigt auf die vom *pname-Parameter* angegebenen Farbtabellenparameterdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie verwenden die Funktionen **glGetColorTableParameterivEXT** und [**glGetColorTableParameterfvEXT,**](glgetcolortableparameterfvext.md) um bestimmte Parameterdaten aus Farbtabellen abzurufen, die mit [**glColorTableEXT**](glcolortableext.md) für Zieltexturpaletten festgelegt wurden. Sie können diese Funktionen auch verwenden, um die Anzahl der Farbtabelleneinträge zu bestimmen, die **glGetColorTableEXT** zurückgibt.

Wenn der *Zielparameter* GL \_ PROXY TEXTURE \_ \_ 1D oder GL \_ PROXY TEXTURE 2D ist und die Implementierung die für \_ format oder \_ *width* angegebenen Werte nicht unterstützt, kann **glColorTableEXT** die angeforderte Farbtabelle nicht erstellen.  In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter sind 0 (null). Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellenformat und eine bestimmte Größe unterstützt, indem **Sie glColorTableEXT** mit einem Proxyziel aufrufen und dann **glGetColorTableParameterivEXT** oder [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glColorTableEXT** festgelegten übereinstimmt. Wenn die abgerufene Breite 0 (null) ist, ist die Farbtabellenanforderung von **glColorTable** fehlgeschlagen. Wenn die abgerufene Breite nicht 0 (null) ist, können Sie **glColorTable** mit dem echten Ziel mit TEXTURE \_ 1D oder TEXTURE \_ 2D aufrufen, um die Farbtabelle festzulegen.

Die Funktionen **glGetColorTableParameterivEXT** und [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) sind Erweiterungsfunktionen, die nicht Teil der OpenGL-Standardbibliothek sind, sondern Teil der GL \_ \_ EXT-Palettentexturerweiterung \_ sind. Um zu überprüfen, ob Ihre Implementierung von OpenGL **glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT** unterstützt, rufen Sie [**glGetString**](glgetstring.md)**(** GL EXTENSIONS \_ )**auf.** Wenn eine GL \_ \_ EXT-Palettentextur zurückgegeben \_ wird, werden **glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT** unterstützt. Rufen Sie [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf, um die Funktionsadresse einer Erweiterungsfunktion abzurufen.

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

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





