---
title: glDrawBuffer-Funktion (Gl.h)
description: Die glDrawBuffer-Funktion gibt an, in welche Farbpuffer gezeichnet werden soll.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5bc715aad24198031ed096d53f1a468b6672532e4df4ae1ef66b416002a65b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081610"
---
# <a name="gldrawbuffer-function"></a>glDrawBuffer-Funktion

Die **glDrawBuffer-Funktion** gibt an, in welche Farbpuffer gezeichnet werden soll.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Gibt bis zu vier Farbpuffer an, in die mit den folgenden zulässigen symbolischen Konstanten gezeichnet werden soll.



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ NONE**</dt> </dl>                                 | Es werden keine Farbpuffer geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ FRONT \_ LEFT**</dt> </dl>              | Es wird nur der Farbpuffer links vorn geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ FRONT \_ RIGHT**</dt> </dl>           | Es wird nur der Rechts-Rechts-Puffer geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ ZURÜCK \_ LINKS**</dt> </dl>                 | Es wird nur der Hintergrund-Links-Farbpuffer geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ ZURÜCK \_ RECHTS**</dt> </dl>              | Es wird nur der Hintergrund-rechts-Farbpuffer geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ FRONT**</dt> </dl>                              | Es werden nur die Farbpuffer "front-left" und "front-right" geschrieben. Wenn kein Farbpuffer rechts von vorne vorn angezeigt wird, wird nur der Puffer für die linke Frontfarbe geschrieben.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ BACK**</dt> </dl>                                 | Es werden nur die Farbpuffer "zurück links" und "zurück rechts" geschrieben. Wenn kein hintergrundrechter Farbpuffer vorüber ist, wird nur der Hintergrund-Links-Farbpuffer geschrieben.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ LEFT**</dt> </dl>                                 | Es werden nur die Farbpuffer "front-left" und "back-left" geschrieben. Wenn kein Hintergrund-Links-Farbpuffer vorüber ist, wird nur der Linke-Hintergrund-Farbpuffer geschrieben.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ RIGHT**</dt> </dl>                              | Es werden nur die Farbpuffer "front-right" und "back-right" geschrieben. Wenn kein Farbpuffer rechts nach rechts angezeigt wird, wird nur der Rechts-Rechts-Puffer geschrieben.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ FRONT \_ AND \_ BACK**</dt> </dl> | Alle Vorder- und Hintergrundfarbpuffer (front-left, front-right, back-left, back-right) werden geschrieben. Wenn es keine Hintergrundfarbpuffer gibt, werden nur die Farbpuffer "front-left" und "front-right" geschrieben. Wenn es keine rechten Farbpuffer gibt, werden nur die Farbpuffer von vorn links und zurück links geschrieben. Wenn keine Rechts- oder Hintergrundfarbpuffer angezeigt werden, wird nur der Farbpuffer links vorn geschrieben.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | Es wird nur der zusätzliche *Farbpuffer i* geschrieben. *i* liegt zwischen 0 und GL \_ AUX \_ BUFFERS - 1. (GL) \_ AUX BUFFERS ist nicht die Obergrenze. Verwenden Sie glGet, um die Anzahl der verfügbaren \_ Hilfspuffer abfragt.) [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)<br/>                                                                                                                            |



 

Der Standardwert ist GL \_ FRONT für Einzelpufferkontexte und GL BACK für doppelt \_ gepufferte Kontexte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Keiner der vom Modus *angegebenen* Puffer war vorhanden.<br/>                                                                           |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |


## <a name="remarks"></a>Hinweise

Wenn Farben in den Framepuffer geschrieben werden, werden sie in die von **glDrawBuffer** angegebenen Farbpuffer geschrieben.

Wenn mehr als ein Farbpuffer zum Zeichnen ausgewählt ist, werden Blending- oder logische Vorgänge unabhängig für jeden Farbpuffer berechnet und angewendet und können in jedem Puffer unterschiedliche Ergebnisse erzeugen.

Monotone Kontexte enthalten nur linke Puffer, und stereotone Kontexte enthalten sowohl linke als auch rechte Puffer. Ebenso enthalten einzelpufferte Kontexte nur Frontpuffer, und doppelt gepufferte Kontexte enthalten sowohl Front- als auch Backpuffer. Der Kontext wird bei der OpenGL-Initialisierung ausgewählt.

Es ist immer der Fall, dass GL \_ AUX *i* = GL \_ AUX0 + *i* ist.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glDrawBuffer-Funktion** ab:

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) dem Argument GL \_ DRAW \_ BUFFER

**glGet** mit argument GL \_ AUX \_ BUFFERS

## <a name="requirements"></a>Requirements (Anforderungen)



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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





