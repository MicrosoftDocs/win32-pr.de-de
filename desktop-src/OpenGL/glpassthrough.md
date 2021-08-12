---
title: glPassThrough-Funktion (Gl.h)
description: Die glPassThrough-Funktion platziert einen Marker im Feedbackpuffer.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5edf1b0fb2dbda1ef1e0a2c4b9ab67b8e7e6305998a8f5a6de9c461e4e148bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615417"
---
# <a name="glpassthrough-function"></a>glPassThrough-Funktion

Die **glPassThrough-Funktion** platziert einen Marker im Feedbackpuffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*token* 
</dt> <dd>

Ein Markerwert, der im Feedbackpuffer platziert werden soll. Sie wird mit dem folgenden eindeutigen Identifizierenswert angegeben.



| Wert                                                                                                                                                                                   | Bedeutung                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_ \_ GL-PASS-THROUGH-TOKEN \_**</dt> </dl> | Die Reihenfolge der **glPassThrough-Befehle** in Bezug auf die Spezifikation von Grafikprimitiven wird beibehalten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Feedback ist ein OpenGL-Rendermodus, der durch Aufrufen von [**glRenderMode**](glrendermode.md) mit GL FEEDBACK ausgewählt \_ wird. Wenn sich OpenGL im Feedbackmodus befindet, werden keine Pixel durch Rasterung erzeugt. Stattdessen werden Informationen zu Primitiven, die gerastert worden wären, von OpenGL an die Anwendung zurückgespeist. Eine Beschreibung des Feedbackpuffers und der darin enthaltenen Werte finden Sie unter [**glFeedbackBuffer.**](glfeedbackbuffer.md)

Die **glPassThrough-Funktion** fügt einen benutzerdefinierten Marker in den Feedbackpuffer ein, wenn er im Feedbackmodus ausgeführt wird. Der *Tokenparameter* wird zurückgegeben, als wäre er ein Primitiver.

Die **glPassThrough-Funktion** wird ignoriert, wenn sich OpenGL nicht im Feedbackmodus befindet.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glPassThrough ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ RENDER \_ MODE

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





