---
title: gldrawbuffer-Funktion (GL. h)
description: Die gldrawbuffer-Funktion gibt an, in welche Farb Puffer gezeichnet werden soll.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- gldrawbuffer-Funktion OpenGL
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
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341591"
---
# <a name="gldrawbuffer-function"></a>gldrawbuffer-Funktion

Die **gldrawbuffer** -Funktion gibt an, in welche Farb Puffer gezeichnet werden soll.

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

Gibt bis zu vier Farb Puffer an, die in mit den folgenden akzeptablen symbolischen Konstanten gezeichnet werden sollen.



| Wert                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ keine**</dt> </dl>                                 | Es wurden keine Farb Puffer geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL- \_ Front- \_ Links**</dt> </dl>              | Nur der Front-Left-Farb Puffer wird geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL- \_ Front- \_ right**</dt> </dl>           | Nur der Front-Right-Farb Puffer wird geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ zurück \_ Links**</dt> </dl>                 | Nur der linke Farb Puffer wird geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ zurück \_ Rechts**</dt> </dl>              | Nur der Hintergrund Farb Puffer wird geschrieben.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL. \_ Front**</dt> </dl>                              | Nur die Front-Left-und Front-Right-Farb Puffer werden geschrieben. Wenn kein Vordergrund rechter Farb Puffer vorhanden ist, wird nur der vordere linke Farb Puffer geschrieben.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ zurück**</dt> </dl>                                 | Es werden nur die Hintergrund-und Hintergrund Farb Puffer geschrieben. Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der Hintergrund Farb Puffer geschrieben.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ Links**</dt> </dl>                                 | Es werden nur die Vorder-und Hintergrundfarben geschrieben. Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der linke Farb Puffer in der Vorderseite geschrieben.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ right**</dt> </dl>                              | Es werden nur die Vorder-und Hintergrundfarben geschrieben. Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der Front-Right-Farb Puffer geschrieben.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ vor \_ und \_ zurück**</dt> </dl> | Alle Vorder-und Hintergrund Farbpuffer (Front-Left, Front-Right, Back-Left, Back-right) werden geschrieben. Wenn keine Hintergrundfarben vorhanden sind, werden nur die Front-Left-und Front-Right-Farb Puffer geschrieben. Wenn keine rechten Farb Puffer vorhanden sind, werden nur die Front-Left-und Back-Left-Farb Puffer geschrieben. Wenn keine Rechte oder Hintergrundfarben Puffer vorhanden sind, wird nur der linke Farb Puffer in der Vorderseite geschrieben.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ Auxi**</dt> </dl>       | Nur der Zusatz Farb Puffer, den *ich geschrieben habe* . der *Wert liegt zwischen* 0 und GL, \_ aux \_ -Puffer-1. (GL \_ AUX- \_ Puffer ist nicht die Obergrenze. verwenden Sie " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die Anzahl der verfügbaren zusätzlichen Puffer abzufragen.)<br/>                                                                                                                            |



 

Der Standardwert ist "GL \_ Front" für Einzel gepufferte Kontexte und "GL \_ Back" für doppelt gepufferte Kontexte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Keiner der durch den *Modus* gekennzeichneten Puffer war vorhanden.<br/>                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |


## <a name="remarks"></a>Bemerkungen

Wenn Farben in den Framebuffer geschrieben werden, werden Sie in die von **gldrawbuffer** angegebenen Farb Puffer geschrieben.

Wenn mehr als ein Farb Puffer zum Zeichnen ausgewählt ist, werden Mischungs-oder logische Operationen berechnet und für jeden Farb Puffer unabhängig voneinander angewendet und können in jedem Puffer zu unterschiedlichen Ergebnissen führen.

Zu den monetischen Kontexten zählen nur linke Puffer, und stereoskopischen Kontexte enthalten sowohl den linken als auch den rechten Puffer. Ebenso umfassen Einzel gepufferte Kontexte nur Front-Puffer, und doppelt gepufferte Kontexte enthalten sowohl den vorderen als auch den Hintergrund Puffer. Der Kontext wird bei der OpenGL-Initialisierung ausgewählt.

Es ist immer der Fall, dass GL \_ aux *i* = GL \_ AUX0 + *i*.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **gldrawbuffer** " ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Zeichnungs \_ Puffer

**glget** mit dem Argument GL \_ aux- \_ Puffer

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

[**glcolormask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glindexmask**](glindexmask.md)
</dt> <dt>

[**gllogicop**](gllogicop.md)
</dt> <dt>

[**glread Buffer**](glreadbuffer.md)
</dt> </dl>

 

 





