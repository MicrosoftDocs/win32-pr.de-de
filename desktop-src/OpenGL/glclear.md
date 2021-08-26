---
title: glClear-Funktion (Gl.h)
description: Die glClear-Funktion gibt Puffer für vordefinierte Werte frei.
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
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082100"
---
# <a name="glclear-function"></a>glClear-Funktion

Die **glClear-Funktion** gibt Puffer für vordefinierte Werte frei.

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

Bitweise OR-Operatoren von Masken, die die zu löschenden Puffer angeben. Die vier Masken lauten wie folgt.



| Wert                                                                                                                                                                                   | Bedeutung                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**GL \_ COLOR \_ BUFFER \_ BIT**</dt> </dl>       | Die Puffer, die derzeit für das Schreiben von Farben aktiviert sind.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**GL \_ DEPTH \_ BUFFER \_ BIT**</dt> </dl>       | Der Tiefenpuffer.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**\_ \_ GL-PUFFERBIT \_**</dt> </dl>       | Der Akkumulationspuffer.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**\_ \_ GL-SCHABLONENPUFFERBIT \_**</dt> </dl> | Der Schablonenpuffer.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Ein anderes Bit als die vier definierten Bits wurde in der Maske *festgelegt.*<br/>                                                                |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glClear-Funktion** legt den Bitebenenbereich des Fensters auf Werte fest, die zuvor von [**glClearColor,**](glclearcolor.md) [**glClearIndex,**](glclearindex.md) [**glClearDepth,**](glcleardepth.md) [**glClearStencil**](glclearstencil.md)und [**glClearAccum**](glclearaccum.md)ausgewählt wurden. Sie können mehrere Farbpuffer gleichzeitig löschen, indem Sie mit [**glDrawBuffer**](gldrawbuffer.md)mehrere Puffer gleichzeitig auswählen.

Der Pixelbesitztest, der Scissor-Test, das Dithering und die Puffer-Schreibmasken wirken sich auf den Betrieb **von glClear aus.** Das Scissor-Feld umrandet den frei werdenden Bereich. Die **glClear-Funktion** ignoriert die Alphafunktion, blend-Funktion, logische Operation, Schablone, Texturzuordnung und *z*-Pufferung.

Die **glClear-Funktion** verwendet ein einzelnes Argument (*mask*), das das bitweise OR mehrerer Werte ist, das angibt, welcher Puffer zu löschen ist.

Der Wert, für den jeder Puffer gepuffert wird, hängt von der Einstellung des eindeutigen Werts für diesen Puffer ab.

Wenn kein Puffer vorhanden ist, hat ein **glClear-Aufruf,** der an diesen Puffer gerichtet ist, keine Auswirkungen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glClear ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument \_ GLGEM \_ CLEAR \_ VALUE

**glGet** mit Argument GL \_ DEPTH \_ CLEAR \_ VALUE

**glGet mit** Argument GL \_ INDEX CLEAR \_ \_ VALUE

**glGet mit** Argument GL \_ COLOR CLEAR \_ \_ VALUE

**glGet** mit Argument GL \_ STENCIL \_ CLEAR \_ VALUE

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





