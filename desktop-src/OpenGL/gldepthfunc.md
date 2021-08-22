---
title: glDepthFunc-Funktion (Gl.h)
description: Die glDepthFunc-Funktion gibt den Wert an, der für Tiefenpuffervergleiche verwendet wird.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229b269e8d9677e0ffdedffb3d91029a473292082409830ac26490bf34680075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617036"
---
# <a name="gldepthfunc-function"></a>glDepthFunc-Funktion

Die **glDepthFunc-Funktion** gibt den Wert an, der für Tiefenpuffervergleiche verwendet wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*func* 
</dt> <dd>

Gibt die Tiefenvergleichsfunktion an. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                   | Bedeutung                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Wird nie durchläuft.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Übergibt, wenn der *eingehende z-Wert* kleiner als der gespeicherte *z-Wert* ist. Dies ist der Standardwert.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Übergibt, wenn der eingehende z-Wert kleiner oder gleich dem gespeicherten z-Wert ist.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Übergibt, wenn der eingehende z-Wert gleich dem gespeicherten z-Wert ist.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Übergibt, wenn der eingehende z-Wert größer als der gespeicherte z-Wert ist.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Übergibt, wenn der eingehende z-Wert nicht gleich dem gespeicherten z-Wert ist.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Übergibt, wenn der eingehende z-Wert größer oder gleich dem gespeicherten z-Wert ist.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Wird immer durchläuft.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glDepthFunc-Funktion** gibt die Funktion an, die verwendet wird, um jeden eingehenden *Pixelwert z* mit dem *z-Wert* im Tiefenpuffer zu vergleichen. Der Vergleich wird nur ausgeführt, wenn Tiefentests aktiviert sind. (Siehe [**glEnable mit**](glenable.md) dem Argument GL \_ \_TIEFENTEST.)

Anfangs sind Tiefentests deaktiviert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glDepthFunc ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ DEPTH \_ FUNC

[**glIsEnabled mit Argument**](glisenabled.md) GL \_ DEPTH \_ TEST

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





