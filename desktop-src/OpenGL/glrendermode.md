---
title: glrendermode-Funktion (GL. h)
description: Die glrendermode-Funktion legt den rasterisierungsmodus fest.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glrendermode-Funktion OpenGL
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
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106197"
---
# <a name="glrendermode-function"></a>glrendermode-Funktion

Die **glrendermode** -Funktion legt den rasterisierungsmodus fest.

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

Der rasterisierungsmodus. Die folgenden drei Werte werden akzeptiert. Der Standardwert ist GL- \_ Rendering.



| Wert                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**GL- \_ Rendering**</dt> </dl>       | Rendermodus. Primitive sind rasterisiert und erzeugen Pixel Fragmente, die in den Framebuffer geschrieben werden. Dies ist der normale Modus und auch der Standardmodus.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ auswählen**</dt> </dl>       | Auswahlmodus. Es werden keine Pixel Fragmente erstellt, und es wird keine Änderung am Frame Puffer-Inhalt vorgenommen. Stattdessen wird ein Datensatz der Namen primitiver Elemente, die gezeichnet würden, wenn der Rendermodus "GL-Rendering" wäre \_ , in einem SELECT-Puffer zurückgegeben, der erstellt werden muss (siehe [**glselectbuffer**](glselectbuffer.md)), bevor der Auswahlmodus eingegeben wird.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**GL- \_ Feedback**</dt> </dl> | Feedback Modus. Es werden keine Pixel Fragmente erstellt, und es wird keine Änderung am Frame Puffer-Inhalt vorgenommen. Stattdessen werden die Koordinaten und Attribute von Vertices, die gezeichnet würden, wenn der Rendermodus "GL-Rendering" wäre \_ , in einem Feedback Puffer zurückgegeben, der erstellt werden muss (siehe [**glfeedbackbuffer**](glfeedbackbuffer.md)), bevor der Feedback Modus eingegeben wird.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war keiner von drei akzeptierten Werten.<br/>                                                                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde mit dem Argument GL \_ SELECT aufgerufen, bevor [**glselectbuffer**](glselectbuffer.md) mindestens einmal aufgerufen wurde.<br/>       |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde mit dem Argument GL \_ Feedback aufgerufen, bevor [**glbeedbackbuffer**](glfeedbackbuffer.md) mindestens einmal aufgerufen wurde.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>       |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glrendermode** " erfordert ein *Argument, das* einen von drei vordefinierten Werten annehmen kann.

Der Rückgabewert der Funktion " **glrendermode** " wird durch den Rendermodus zum Zeitpunkt des Aufrufs von " **glrendermode** " und nicht durch den *Modus* bestimmt. Die folgenden Werte werden für die drei Rendermodi zurückgegeben:



| Wert        | Bedeutung                                                                 |
|--------------|-------------------------------------------------------------------------|
| GL- \_ Rendering   | Keinen.                                                                   |
| GL \_ auswählen   | Die Anzahl der Treffer Datensätze, die an den ausgewählten Puffer übertragen werden.             |
| GL- \_ Feedback | Die Anzahl der Werte (keine Scheitel Punkte), die in den Feedback Puffer übertragen werden. |



 

Weitere Informationen zum Vorgang zur Auswahl und zum Feedback finden Sie unter " [**glselectbuffer**](glselectbuffer.md) " und " [**glfeedbackbuffer**](glfeedbackbuffer.md) ".

Wenn ein Fehler generiert wird, gibt **glrendermode unabhängig vom aktuellen Rendermodus** 0 zurück.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glrendermode** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glfeedbackbuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glinitnames**](glinitnames.md)
</dt> <dt>

[**glloadname**](glloadname.md)
</dt> <dt>

[**glpassthrough**](glpassthrough.md)
</dt> <dt>

[**glpushname**](glpushname.md)
</dt> <dt>

[**glselectbuffer**](glselectbuffer.md)
</dt> </dl>

 

 





