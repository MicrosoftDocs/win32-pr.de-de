---
title: glgetcolortableparameterivext-Funktion (GL. h)
description: Die Funktionen "glgetcolortableparameterfvext" und "glgetcolortableparameterivext" erhalten palettenparameter aus Farbtabellen. | glgetcolortableparameterivext-Funktion (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glgetcolortableparameterivext-Funktion OpenGL
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
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351897"
---
# <a name="glgetcolortableparameterivext-function"></a>glgetcolortableparameterivext-Funktion

Die Funktionen " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) " und " **glgetcolortableparameterivext** " erhalten palettenparameter aus Farbtabellen.

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

Die Ziel Textur der Palette, für die Sie Parameterdaten benötigen. Muss Textur \_ 1D, Textur \_ 2D, Proxy \_ Textur \_ 1D oder Proxy \_ Textur \_ 2D sein.

</dd> <dt>

*pName* 
</dt> <dd>

Eine symbolische Konstante für den Typ der palettenparameterdaten, auf die von *para* Metern verwiesen wird.

Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.



| Wert                                                                                                                                                                                                             | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL- \_ Farb \_ Tabellen Format ( \_ \_ ext)**</dt> </dl>              | Gibt das interne Format zurück, das durch den letzten Aufrufe von [**glcolortableext**](glcolortableext.md) oder den Standardwert angegeben wird.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL- \_ Farb \_ Tabellenbreite ( \_ \_ ext)**</dt> </dl>                 | Gibt die Breite der aktuellen Palette zurück.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ Color \_ Table \_ Red \_ size \_ ext**</dt> </dl>       | Gibt die tatsächliche Größe zurück, die intern verwendet wird, um die rote Komponente der Palettendaten zu speichern.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ Color \_ Table \_ Green \_ size \_ ext**</dt> </dl> | Gibt die tatsächliche Größe zurück, die zum Speichern der grünen Komponente der Palettendaten intern verwendet wird.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ Color \_ Table \_ Blue \_ size \_ ext**</dt> </dl>    | Gibt die tatsächliche Größe zurück, die intern verwendet wird, um die blaue Komponente der Palettendaten zu speichern.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ Color \_ Table \_ alpha \_ size \_ ext**</dt> </dl> | Gibt die tatsächliche Größe zurück, die zum Speichern der Alpha Komponente der Palettendaten intern verwendet wird.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Verweist auf die farbtabellenparameterdaten, die durch den *PName* -Parameter angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktionen " **glgetcolortableparameterivext** " und " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) ", um bestimmte Parameterdaten aus Farbtabellen abzurufen, die mit " [**glcolortableext**](glcolortableext.md) " für gezielte Textur Paletten festgelegt sind. Außerdem können Sie diese Funktionen verwenden, um die Anzahl der Farb Tabelleneinträge zu bestimmen, die von **glgetcolortableext** zurückgegeben werden.

Wenn der *Ziel* Parameter GL- \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D ist, und die-Implementierung die für *Format* oder *Width* angegebenen Werte nicht unter  stützt, kann bei der Erstellung der angeforderten Farbtabelle ein Fehler auftreten. In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter haben den Wert 0 (null). Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellen Format und eine bestimmte Größe unterstützt, indem Sie **glcolortableext** mit einem Proxy Ziel aufrufen und dann **glgetcolortableparameterivext** oder [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glcolortableext** festgelegten width-Parameter übereinstimmt. Wenn die abgerufene Breite 0 (null) ist, ist die Farbtabellen Anforderung von **glcolortable** fehlgeschlagen. Wenn die abgerufene Breite nicht NULL ist, können Sie **glcolortable** mit dem echten Ziel mit Textur \_ 1D oder Textur \_ 2D zum Festlegen der Farbtabelle abrufen.

Die Funktionen " **glgetcolortableparameterivext** " und " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) " sind Erweiterungsfunktionen, die nicht Teil der OpenGL-Standardbibliothek sind, aber Teil der Erweiterung "GL \_ Ext- \_ \_ Textur Erweiterung" sind. Um zu überprüfen, ob die Implementierung von OpenGL **glgetcolortableparameterivext** und **glgetcolortableparameterfvext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)**(** GL \_ Extensions **)**. Wenn Sie \_ die Struktur von GL Ext \_ -Struktur zurückgibt \_ , werden **glgetcolortableparameterivext** und **glgetcolortableparameterfvext** unterstützt. Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.

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

[**glgetcolortableext**](glgetcolortableext.md)
</dt> <dt>

[**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





