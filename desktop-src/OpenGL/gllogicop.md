---
title: gllogicop-Funktion (GL. h)
description: Die Funktion "gllogicop" gibt einen logischen Pixel Vorgang für das Rendern von Farbindizes an.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- gllogicop-Funktion OpenGL
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
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519151"
---
# <a name="gllogicop-function"></a>gllogicop-Funktion

Die Funktion " **gllogicop** " gibt einen logischen Pixel Vorgang für das Rendern von Farbindizes an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OpCode* 
</dt> <dd>

Eine symbolische Konstante, die eine logische Operation auswählt. Die folgenden Symbole werden akzeptiert, wenn s dem Wert des Quell Bits entspricht und d der Wert des Zielbits ist.



| Wert                                                                                                                                                                   | Bedeutung              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ Clear**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**GL- \_ Satz**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**GL- \_ Kopie**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**GL- \_ Kopie \_ invertiert**</dt> </dl> | ! s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL. \_ NoOp**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ Invert**</dt> </dl>                       | ! d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ und**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ .**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ oder**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ .**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL. \_ Xor**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL- \_ equiv**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ und \_ umgekehrt**</dt> </dl>       | s &! d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ und \_ invertiert**</dt> </dl>    | ! s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ oder \_ umgekehrt**</dt> </dl>          | s \| ! d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ oder \_ invertiert**</dt> </dl>       | ! s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Opcode* war kein akzeptierter Wert.<br/>                                                                                        |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **gllogicop** " gibt eine logische Operation an, die bei Aktivierung zwischen dem eingehenden Farb Index und dem Farb Index an der entsprechenden Position im Framebuffer angewendet wird. Die logische Operation wird mit " [**glEnable**](glenable.md) " und " **glEnable** " mithilfe der symbolischen Konstante "GL Logic op" aktiviert oder deaktiviert \_ \_ .

Der *Opcode* -Parameter ist eine symbolische Konstante, die aus der nachstehenden Liste ausgewählt wird. In der Erläuterung der logischen Vorgänge stellt *s* den eingehenden Farbindex und *d* den Index im Framebuffer dar. Standard-C-sprach Operatoren werden verwendet. Wie diese bitweisen Operatoren vorschlagen, wird die logische Operation unabhängig von jedem bitpaar der Quell-und Ziel Indizes angewendet.

Logische Pixel Vorgänge werden nicht auf RGBA-Farb Puffer angewendet.

Wenn mehr als ein Farb Index Puffer für das Zeichnen aktiviert ist, werden logische Vorgänge für jeden aktivierten Puffer separat durchgeführt, wobei der Inhalt dieses Puffers für den Zielindex verwendet wird (siehe [**gldrawbuffer**](gldrawbuffer.md)).

Der *Opcode* -Parameter muss einer der 16 akzeptierten Werte sein. Andere Werte führen zu einem Fehler.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gllogicop** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Logic \_ op \_ Mode

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Logic \_ op

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

[**glalphafunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**gldrawbuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> </dl>

 

 





