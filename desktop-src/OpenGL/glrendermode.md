---
title: glRenderMode-Funktion (Gl.h)
description: Die glRenderMode-Funktion legt den Rastermodus fest.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93eb3c7e2d7f4a6d261632e0f010cf0e1c7a2410a5a8364a6cf1fd65f36ada99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777930"
---
# <a name="glrendermode-function"></a>glRenderMode-Funktion

Die **glRenderMode-Funktion** legt den Rastermodus fest.

## <a name="syntax"></a>Syntax


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Der Rasterungsmodus. Die folgenden drei Werte werden akzeptiert. Der Standardwert ist GL \_ RENDER.



| Wert                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**GL \_ RENDER**</dt> </dl>       | Rendermodus. Primitive werden rasterisiert und erzeugen Pixelfragmente, die in den Framepuffer geschrieben werden. Dies ist der normale Modus und auch der Standardmodus.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ SELECT**</dt> </dl>       | Auswahlmodus. Es werden keine Pixelfragmente erstellt, und es werden keine Änderungen am Framepufferinhalt vorgenommen. Stattdessen wird ein Datensatz der Namen primitiver Typen, die gezeichnet worden wären, wenn der Rendermodus GL RENDER wäre, in einem Select-Puffer zurückgegeben, der erstellt werden muss \_ (siehe [**glSelectBuffer**](glselectbuffer.md)), bevor der Auswahlmodus aktiviert wird.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**GL \_ FEEDBACK**</dt> </dl> | Feedbackmodus. Es werden keine Pixelfragmente erstellt, und es werden keine Änderungen am Framepufferinhalt vorgenommen. Stattdessen werden die Koordinaten und Attribute von Scheitelungen, die gezeichnet worden wären, wenn der Rendermodus GL RENDER wäre, in einem Feedbackpuffer zurückgegeben, der erstellt werden muss \_ (siehe [**glFeedbackBuffer),**](glfeedbackbuffer.md)bevor der Feedbackmodus aktiviert wird.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war nicht einer von drei akzeptierten Werten.<br/>                                                                                     |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde mit dem Argument GL \_ SELECT aufgerufen, bevor [**glSelectBuffer**](glselectbuffer.md) mindestens einmal aufgerufen wurde.<br/>       |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde mit dem Argument GL \_ FEEDBACK aufgerufen, bevor [**glBeedbackBuffer**](glfeedbackbuffer.md) mindestens einmal aufgerufen wurde.<br/> |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>       |



## <a name="remarks"></a>Hinweise

Die **glRenderMode-Funktion** verwendet ein Argument, *mode*, das einen von drei vordefinierten Werten oben annehmen kann.

Der Rückgabewert der **glRenderMode-Funktion** wird durch den Rendermodus zum Zeitpunkt des Aufrufens **von glRenderMode** und nicht durch den Modus *bestimmt.* Die für die drei Rendermodi zurückgegebenen Werte lauten wie folgt.



| Wert        | Bedeutung                                                                 |
|--------------|-------------------------------------------------------------------------|
| GL \_ RENDER   | Keinen.                                                                   |
| GL \_ SELECT   | Die Anzahl der Trefferdatensätze, die an den Ausgewählten Puffer übertragen werden.             |
| GL \_ FEEDBACK | Die Anzahl der Werte (nicht Scheitelzeichen), die an den Feedbackpuffer übertragen werden. |



 

Weitere Informationen zum Auswahl- und Feedbackvorgang finden Sie unter [**glSelectBuffer**](glselectbuffer.md) und [**glFeedbackBuffer.**](glfeedbackbuffer.md)

Wenn ein Fehler generiert wird, **gibt glRenderMode** unabhängig vom aktuellen Rendermodus null zurück.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glRenderMode ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ RENDER \_ MODE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





