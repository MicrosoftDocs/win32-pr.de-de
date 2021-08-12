---
title: glStencilOp-Funktion (Gl.h)
description: Die glStencilOp-Funktion legt die Schablonentestaktionen fest.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da899207456cece58216874c7540a032326e4180e9484590e2effd619eea72f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614334"
---
# <a name="glstencilop-function"></a>glStencilOp-Funktion

Die **glStencilOp-Funktion** legt die Schablonentestaktionen fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* 
</dt> <dd>

Die Aktion, die durchgeführt werden soll, wenn der Schablonentest fehlschlägt. Die folgenden sechs symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                | Bedeutung                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ KEEP**</dt> </dl>          | Behält den aktuellen Wert bei.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ ZERO**</dt> </dl>          | Legt den Schablonenpufferwert auf 0 (null) fest.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ REPLACE**</dt> </dl> | Legt den Schablonenpufferwert auf *ref* fest, wie von **glStencilFunc angegeben.**<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL \_ INCR**</dt> </dl>          | Erhöht den aktuellen Schablonenpufferwert. Klammern an den maximal darstellbaren Wert ohne Vorzeichen.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ DECR**</dt> </dl>          | Dekrementiert den aktuellen Schablonenpufferwert. Klammern auf 0 (null).<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>    | Bitweises Invertiert den aktuellen Schablonenpufferwert.<br/>                                                |



 

</dd> <dt>

*-Nistail* 
</dt> <dd>

Schablonenaktion, wenn der Schablonentest bestanden wird, der Tiefentest jedoch fehlschlägt. Akzeptiert die gleichen symbolischen Konstanten wie *fail.*

</dd> <dt>

*zpass* 
</dt> <dd>

Schablonenaktion, wenn sowohl der Schablonentest als auch der Tiefentest bestanden werden oder wenn der Schablonentest bestanden wird und entweder kein Tiefenpuffer oder keine Tiefentests aktiviert sind. Akzeptiert die gleichen symbolischen Konstanten wie *fail.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      |  *fail,ggail* oder *zpass* war ein beliebiger Wert, der nicht die sechs definierten konstanten Werte war.<br/>                                      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Schablonen, wie *z*-buffering, ermöglichen und deaktivieren das Zeichnen pro Pixel. Sie zeichnen mit OpenGL-Zeichnungsprimitiven in die Schablonenebenen und rendern dann Geometrie und Bilder, indem Sie die Schablonenebenen verwenden, um Teile des Bildschirms zu maskieren. Schablonen werden in der Regel in Multipass-Renderingalgorithmen verwendet, um Sondereffekte zu erzielen, wie z. B. Abschärfungen, Lining und das rendern von solider Geometrie.

Der Schablonentest entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Wert im Schablonenpuffer und einem Verweiswert. Der Test wird mit [**glEnable-**](glenable.md) und [**glDisable-Aufrufen**](gldisable.md) mit dem Argument GL STENCIL TEST aktiviert und mit \_ \_ [**glStencilFunc gesteuert.**](glstencilfunc.md)

Die **glStencilOp-Funktion** verwendet drei Argumente, die angeben, was mit dem gespeicherten Schablonenwert geschieht, während die Schablone aktiviert ist. Wenn der Schablonentest fehlschlägt, wird keine Änderung an der Farbe oder den Tiefenpuffern des Pixels vorgenommen, und *fail* gibt an, was mit dem Inhalt des Schablonenpuffers geschieht.

Schablonenpufferwerte werden als ganze Zahlen ohne Vorzeichen behandelt. Wenn sie inkrementiert und dekrementiert werden, werden werte an 0 und 2 *n* 1 geklammert, wobei *n* der Wert ist, der durch Abfragen von GL \_ STENCIL BITS zurückgegeben \_ wird.

Die anderen beiden Argumente für **glStencilOp** geben Schablonenpufferaktionen an, wenn nachfolgende Tiefenpuffertests erfolgreich sind (*zpass*) oder fehlschlagen (*): ).* (Siehe [**glDepthFunc**](gldepthfunc.md).) Sie werden mit den gleichen sechs symbolischen Konstanten wie fail *angegeben.* Beachten *Sie, dass eine* Dämpfung ignoriert wird, wenn kein Tiefenpuffer vorüber ist oder wenn der Tiefenpuffer nicht aktiviert ist. In diesen Fällen geben *fail* und *zpass* die Schablonenaktion an, wenn der Schablonentest fehlschlägt bzw. bestanden wird.

Der Schablonentest ist anfänglich deaktiviert. Wenn es keinen Schablonenpuffer gibt, kann keine Schablonenänderung erfolgen, und es ist so, als ob die Schablonentests immer bestanden würden, unabhängig von jedem Aufruf von **glStencilOp**.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glStencilOp ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ STENCIL \_ FAIL

**glGet** mit Argument GL \_ STENCIL \_ PASS DEPTH \_ \_ PASS

**glGet** mit Argument GL \_ STENCIL \_ PASS DEPTH \_ \_ FAIL

**glGet** mit Argument GL \_ STENCIL \_ BITS

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ STENCIL \_ TEST

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





