---
title: glGetColorTableParameterfvEXT-Funktion (Gl.h)
description: Die Funktionen glGetColorTableParameterfvEXT und glGetColorTableParameterivEXT erhalten Palettenparameter aus Farbtabellen. | glGetColorTableParameterfvEXT-Funktion (Gl.h)
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- glGetColorTableParameterfvEXT-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7cd93c45c602b35e88fe28c467943829669d329f75007607783ece06f1b51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615770"
---
# <a name="glgetcolortableparameterfvext-function"></a>glGetColorTableParameterfvEXT-Funktion

Die **Funktionen glGetColorTableParameterfvEXT** und [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) erhalten Palettenparameter aus Farbtabellen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur der Palette, für die Sie Parameterdaten verwenden möchten. Muss TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D oder PROXY \_ TEXTURE \_ 2D sein.

</dd> <dt>

*pname* 
</dt> <dd>

Eine symbolische Konstante für den Typ der Palettenparameterdaten, auf die von *Parametern verwiesen wird.*

Im Folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutungen.



| Wert                                                                                                                                                                                                             | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ FORMAT \_ EXT**</dt> </dl>              | Gibt das interne Format zurück, das durch den letzten Aufruf von [**glColorTableEXT**](glcolortableext.md) oder dem Standardwert angegeben wurde.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ WIDTH \_ EXT**</dt> </dl>                 | Gibt die Breite der aktuellen Palette zurück.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ RED \_ SIZE \_ EXT**</dt> </dl>       | Gibt die tatsächliche Größe zurück, die intern zum Speichern der roten Komponente der Palettendaten verwendet wird.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ GREEN \_ SIZE \_ EXT**</dt> </dl> | Gibt die tatsächliche Größe zurück, die intern zum Speichern der grünen Komponente der Palettendaten verwendet wird.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ BLUE \_ SIZE \_ EXT**</dt> </dl>    | Gibt die tatsächliche Größe zurück, die intern zum Speichern der blauen Komponente der Palettendaten verwendet wird.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ ALPHA \_ SIZE \_ EXT**</dt> </dl> | Gibt die tatsächliche Größe zurück, die intern zum Speichern der Alphakomponente der Palettendaten verwendet wird.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Zeigt auf die Vom *pname-Parameter* angegebenen Farbtabellenparameterdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie verwenden **die Funktionen glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT,** um bestimmte Parameterdaten aus Farbtabellen abzurufen, die mit [**glColorTableEXT**](glcolortableext.md) für Zieltexturpaletten festgelegt wurden. Sie können diese Funktionen auch verwenden, um die Anzahl der Farbtabelleneinträge zu bestimmen, die **glGetColorTableEXT zurückgibt.**

Wenn  der Zielparameter GL PROXY TEXTURE 1D oder GL PROXY TEXTURE 2D ist und die Implementierung die für format oder width angegebenen Werte nicht unterstützt, kann \_ \_ \_ \_ \_ \_ **glColorTableEXT**  die angeforderte Farbtabelle nicht erstellen. In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter sind 0 (null). Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellenformat und eine bestimmte Größe unterstützt, indem Sie **glColorTableEXT** mit einem Proxyziel aufrufen und **dann glGetColorTableParameterivEXT** oder **glGetColorTableParameterfvEXT** aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glColorTableEXT** festgelegten -Parameter entspricht. Wenn die abgerufene Breite 0 (null) ist, ist die Anforderung der Farbtabelle **durch glColorTable** fehlgeschlagen. Wenn die abgerufene Breite nicht 0 (null) ist, können Sie **glColorTable** mit dem echten Ziel mit TEXTURE 1D oder TEXTURE 2D aufrufen, um die \_ \_ Farbtabelle festlegen.

Die **Funktionen glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT** sind Erweiterungsfunktionen, die nicht Teil der OpenGL-Standardbibliothek sind, aber Teil der GL EXT-Texturerweiterung mit Palette \_ \_ \_ sind. Um zu überprüfen, ob Ihre OpenGL-Implementierung **glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT** unterstützt, rufen Sie [**glGetString**](glgetstring.md)**(** GL EXTENSIONS \_ )**auf.** Wenn die GL \_ \_ EXT-Palettentextur \_ zurückgegeben wird, **werden glGetColorTableParameterivEXT** und **glGetColorTableParameterfvEXT** unterstützt. Um die Funktionsadresse einer Erweiterungsfunktion zu erhalten, rufen [**Sie wglGetProcAddress auf.**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)

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

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





