---
title: glalphafunc-Funktion (GL. h)
description: Die glalphafunc-Funktion ermöglicht der Anwendung das Festlegen der Alpha-Testfunktion.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glalphafunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342021"
---
# <a name="glalphafunc-function"></a>glalphafunc-Funktion

Die **glalphafunc** -Funktion ermöglicht der Anwendung das Festlegen der Alpha-Testfunktion.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*func* 
</dt> <dd>

Die Alpha Vergleichsfunktion. Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.



| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nie**</dt> </dl>          | Läuft nie ab.<br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ weniger**</dt> </dl>             | Übergibt, wenn der eingehende Alpha-Wert kleiner als der Verweis Wert ist.<br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ gleich**</dt> </dl>          | Übergibt, wenn der eingehende Alpha Wert gleich dem Verweis Wert ist.<br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ lequal**</dt> </dl>       | Übergibt, wenn der eingehende Alpha-Wert kleiner oder gleich dem Verweis Wert ist.<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ größer**</dt> </dl>    | Übergibt, wenn der eingehende Alpha-Wert größer als der Verweis Wert ist.<br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL- \_ NotEqual**</dt> </dl> | Übergibt, wenn der eingehende Alpha Wert nicht gleich dem Verweis Wert ist.<br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ gequal**</dt> </dl>       | Übergibt, wenn der eingehende Alpha-Wert größer oder gleich dem Verweis Wert ist.<br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**immer GL. \_**</dt> </dl>       | Übergibt immer. Dies ist die Standardoption.<br/>                                                 |



 

</dd> <dt>

*ref* 
</dt> <dd>

Der Verweis Wert, mit dem eingehende Alpha Werte verglichen werden. Dieser Wert wird an den Bereich von 0 bis 1 gebunden, wobei 0 den niedrigsten möglichen Alpha-Wert und 1 den höchstmöglichen Wert darstellt. Der Standard Verweis ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *Func* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Der Alpha Test verwirft Fragmente abhängig vom Ergebnis eines Vergleichs zwischen den Alpha Werten der eingehenden Fragmente und einem konstanten Verweis Wert. Die Funktion " **glalphafunc** " gibt den Verweis und die Vergleichsfunktion an. Der Vergleich wird nur durchgeführt, wenn Alpha Tests aktiviert ist. (Weitere Informationen zu GL \_ Alpha \_ Test, siehe [**glEnable**](glenable.md).)

Der *Func* -Parameter und der *ref* -Parameter geben die Bedingungen an, unter denen das Pixel gezeichnet wird. Der eingehende Alpha-Wert wird *mit der* -Funktion verglichen, die von *Func* angegeben wird. Wenn der Vergleich bestanden wird, wird das eingehende Fragment gezeichnet, bedingt bei nachfolgenden Schablonen-und tiefen Puffer Tests. Wenn der Vergleich fehlschlägt, erfolgt keine Änderung am Frame Puffer an dieser Pixelposition.

Die **glalphafunc** -Funktion arbeitet mit allen Pixel Schreibvorgängen, einschließlich derjenigen, die sich aus der Scan Konvertierung von Punkten, Zeilen, Polygonen und Bitmaps ergeben, sowie aus Pixel Zeichnungs-und Kopier Vorgängen. Die **glalphafunc** -Funktion wirkt sich nicht auf Bildschirm Löschvorgänge aus.

Alpha Tests werden nur im RGBA-Modus ausgeführt.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glalphafunc** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ alpha \_ Test \_ Func

**glget** mit Argument GL \_ alpha \_ Test \_ Ref

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ alpha \_ Test

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

[**glblendfunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> </dl>

 

 





