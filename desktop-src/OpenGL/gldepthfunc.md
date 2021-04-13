---
title: gldepthfunc-Funktion (GL. h)
description: Die Funktion "gldepthfunc" gibt den Wert an, der für tiefen Puffer Vergleiche verwendet wird.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- gldepthfunc-Funktion OpenGL
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
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475843"
---
# <a name="gldepthfunc-function"></a>gldepthfunc-Funktion

Die Funktion " **gldepthfunc** " gibt den Wert an, der für tiefen Puffer Vergleiche verwendet wird.

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

Gibt die Tiefe Vergleichsfunktion an. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                   | Bedeutung                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nie**</dt> </dl>          | Läuft nie ab.<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ weniger**</dt> </dl>             | Übergibt, wenn der eingehende *z* -Wert kleiner als der gespeicherte *z* -Wert ist. Dies ist der Standardwert.<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ lequal**</dt> </dl>       | Übergibt, wenn der eingehende z-Wert kleiner oder gleich dem gespeicherten z-Wert ist.<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ gleich**</dt> </dl>          | Übergibt, wenn der eingehende z-Wert gleich dem gespeicherten z-Wert ist.<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ größer**</dt> </dl>    | Übergibt, wenn der eingehende z-Wert größer als der gespeicherte z-Wert ist.<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL- \_ NotEqual**</dt> </dl> | Übergibt, wenn der eingehende z-Wert nicht gleich dem gespeicherten z-Wert ist.<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ gequal**</dt> </dl>       | Übergibt, wenn der eingehende z-Wert größer oder gleich dem gespeicherten z-Wert ist.<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**immer GL. \_**</dt> </dl>       | Übergibt immer.<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **gldepthfunc** " gibt die Funktion an, mit der die einzelnen eingehenden Pixel- *z* -Werte mit dem im tiefen Puffer vorhandenen *z* -Wert verglichen werden. Der Vergleich wird nur durchgeführt, wenn tiefen Tests aktiviert sind. (Siehe [**glEnable**](glenable.md) mit dem Argument GL \_ . tiefen \_ Test.)

Zunächst sind die tiefen Tests deaktiviert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gldepthfunc** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Tiefe \_ Func

[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ tiefen \_ Test

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

[**gldepthrange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





