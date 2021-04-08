---
title: glpassthrough-Funktion (GL. h)
description: Die Funktion "glpassthrough" platziert einen Marker im Feedback Puffer.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glpassthrough-Funktion OpenGL
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
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741136"
---
# <a name="glpassthrough-function"></a>glpassthrough-Funktion

Die Funktion " **glpassthrough** " platziert einen Marker im Feedback Puffer.

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

Ein Markerwert, der in den Feedback Puffer eingefügt werden soll. Dies wird durch den folgenden eindeutigen identifizierenden Wert angegeben.



| Wert                                                                                                                                                                                   | Bedeutung                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**GL- \_ Pass- \_ through- \_ Token**</dt> </dl> | Die Reihenfolge der **glpassthrough** -Befehle in Bezug auf die Spezifikation von Grafik primitiven wird beibehalten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Feedback ist ein OpenGL-Rendermodus, der durch Aufrufen von [**glrendermode**](glrendermode.md) mit GL-Feedback ausgewählt wird \_ . Wenn OpenGL im Feedback Modus ist, werden von der rasterisierung keine Pixel erzeugt. Stattdessen werden Informationen über primitive, die gerengt worden wären, von OpenGL an die Anwendung zurückgegeben. Eine Beschreibung des Feedback Puffers und der darin verwendeten Werte finden Sie unter [**glfeedbackbuffer**](glfeedbackbuffer.md) .

Die **glpassthrough** -Funktion fügt einen benutzerdefinierten Marker in den Feedback Puffer ein, wenn er im Feedback Modus ausgeführt wird. Der *tokenparameter* wird zurückgegeben, als ob es sich um einen primitiven handelt.

Die **glpassthrough** -Funktion wird ignoriert, wenn OpenGL nicht im Feedback Modus ist.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glpassthrough** ab:

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

[**glrendermode**](glrendermode.md)
</dt> </dl>

 

 





