---
title: glClear-Funktion (GL. h)
description: Die Funktion "glClear" löscht Puffer in voreingestellten Werte.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338740"
---
# <a name="glclear-function"></a>glClear-Funktion

Die Funktion " **glClear** " löscht Puffer in voreingestellten Werte.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Bitweise OR-Operatoren von Masken, die die zu löschenden Puffer angeben. Die vier Masken sind wie folgt.



| Wert                                                                                                                                                                                   | Bedeutung                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**GL- \_ Farb \_ Puffer \_ Bit**</dt> </dl>       | Die aktuell für das Schreiben von Farben aktivierten Puffer.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**GL- \_ Tiefe- \_ Puffer \_ Bit**</dt> </dl>       | Der tiefen Puffer.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**GL- \_ Accum- \_ Puffer \_ Bit**</dt> </dl>       | Der Akkumulations Puffer.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**GL- \_ Schablone- \_ Puffer \_ Bit**</dt> </dl> | Der Schablonen Puffer.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Alle anderen Bits als die vier definierten Bits wurden in *Mask* festgelegt.<br/>                                                                |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Mit der Funktion " **glClear** " wird der bitplane-Bereich des Fensters auf Werte festgelegt, die zuvor von [**glclearcolor**](glclearcolor.md), [**glclearindex**](glclearindex.md), [**glcleartiefe**](glcleardepth.md), [**glclearstencil**](glclearstencil.md)und [**glclearaccum**](glclearaccum.md)ausgewählt wurden. Sie können mehrere Farb Puffer gleichzeitig löschen, indem Sie mit [**gldrawbuffer**](gldrawbuffer.md)mehr als einen Puffer gleichzeitig auswählen.

Der Pixel Besitz Test, die Scheren-Tests, die Dithering-und die Buffer-Schreibvorgänge wirken sich auf den Vorgang von **glClear** aus. Das Feld "Scheren" grenzt den gelöschten Bereich an. Die Funktion " **glClear** " ignoriert die Funktionen "Alpha", "Blend", "logischer Vorgang", "Schablone", "Textur Zuordnung" und " *z*-Pufferung".

Die Funktion " **glClear** " hat ein einzelnes Argument (*Mask*), bei dem es sich um das bitweise OR von mehreren Werten handelt, die angeben, welcher Puffer gelöscht werden soll.

Der Wert, auf den der Puffer gelöscht wird, hängt von der Einstellung des Clear-Werts für diesen Puffer ab.

Wenn kein Puffer vorhanden ist, hat ein **glClear** -Befehl, der an diesen Puffer gerichtet ist, keine Auswirkung.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glClear** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value

**glget** mit Argument GL- \_ Tiefe \_ Clear- \_ Wert

**glget** mit Argument GL- \_ Index \_ Clear- \_ Wert

**glget** mit dem Argument GL \_ Color \_ Clear \_ value

**glget** mit dem Argument GL \_ Stencil \_ Clear \_ value

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

[**glclearaccum**](glclearaccum.md)
</dt> <dt>

[**glclearcolor**](glclearcolor.md)
</dt> <dt>

[**glcleartiefe**](glcleardepth.md)
</dt> <dt>

[**glclearindex**](glclearindex.md)
</dt> <dt>

[**glclearstencil**](glclearstencil.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glscissor**](glscissor.md)
</dt> </dl>

 

 





