---
title: glLogicOp-Funktion (Gl.h)
description: Die glLogicOp-Funktion gibt einen logischen Pixelvorgang für das Farbindexrendering an.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427bd338e416843418fa7551d4e1632dccaf268426ca2a910e164aeae50663dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492670"
---
# <a name="gllogicop-function"></a>glLogicOp-Funktion

Die **glLogicOp-Funktion** gibt einen logischen Pixelvorgang für das Farbindexrendering an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*opcode* 
</dt> <dd>

Eine symbolische Konstante, die einen logischen Vorgang auswählt. Die folgenden Symbole werden akzeptiert, wobei s gleich dem Wert des Quellbits und d der Wert des Zielbits ist.



| Wert                                                                                                                                                                   | Bedeutung              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ CLEAR**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**GL \_ SET**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**GL \_ COPY**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**GL \_ COPY \_ INVERTED**</dt> </dl> | !s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL \_ NOOP**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>                       | !d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ UND**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ ODER**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ NOR**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL \_ XOR**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ EQUIV**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ UND \_ REVERSE**</dt> </dl>       | s & !d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ UND \_ INVERTED**</dt> </dl>    | !s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ ODER \_ REVERSE**</dt> </dl>          | s \| !d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ ODER \_ INVERTED**</dt> </dl>       | !s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *opcode* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glLogicOp-Funktion** gibt einen logischen Vorgang an, der bei Aktivierung zwischen dem eingehenden Farbindex und dem Farbindex an der entsprechenden Position im Framepuffer angewendet wird. Der logische Vorgang wird mit [**glEnable**](glenable.md) und **glDisable** mithilfe der symbolischen Konstanten GL LOGIC OP aktiviert oder \_ \_ deaktiviert.

Der *Opcode-Parameter* ist eine symbolische Konstante, die aus der folgenden Liste ausgewählt wird. In der Erläuterung der logischen Vorgänge stellt *s* den eingehenden Farbindex und *d* den Index im Framepuffer dar. Es werden C-Standardsprachoperatoren verwendet. Wie diese bitweisen Operatoren vermuten, wird der logische Vorgang unabhängig auf jedes Bitpaar der Quell- und Zielindizes angewendet.

Logische Pixelvorgänge werden nicht auf RGBA-Farbpuffer angewendet.

Wenn mehr als ein Farbindexpuffer für das Zeichnen aktiviert ist, werden logische Vorgänge separat für jeden aktivierten Puffer ausgeführt, wobei der Inhalt dieses Puffers für den Zielindex verwendet wird (siehe [**glDrawBuffer**](gldrawbuffer.md)).

Der *opcode-Parameter* muss einer der 16 akzeptierten Werte sein. Andere Werte führen zu einem Fehler.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLogicOp** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ LOGIC \_ OP \_ MODE

[**glIsEnabled**](glisenabled.md) mit argument GL \_ LOGIC \_ OP

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





