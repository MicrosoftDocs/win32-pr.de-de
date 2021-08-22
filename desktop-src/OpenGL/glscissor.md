---
title: glScissor-Funktion (Gl.h)
description: Die glScissor-Funktion definiert das Scissor-Feld.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor-Funktion OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fafefaaaa3315679af2900808f581324040512816dd2211a0250375c36f824dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777820"
---
# <a name="glscissor-function"></a>glScissor-Funktion

Die **glScissor-Funktion** definiert das Scissor-Feld.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die x-Koordinate (vertikale Achse) für die untere linke Ecke des Scissor-Felds.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Koordinate (horizontale Achse) für die untere linke Ecke des Scissor-Felds. Zusammen geben x und y die untere linke Ecke des Scissor-Felds an. Anfänglich (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Scissor-Felds.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Scissor-Felds. Wenn ein OpenGL-Kontext *zum ersten* Mal an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                   |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glScissor-Funktion** definiert ein Rechteck, das als Scissor-Feld bezeichnet wird, in Fensterkoordinaten. Die ersten beiden Parameter , *x* und *y,* geben die untere linke Ecke des Felds an. Die *Parameter width* und *height* geben die Breite und Höhe des Felds an.

Der Scissor-Test ist mit [**glEnable**](glenable.md) und **glDisable** mit dem Argument GL SCISSOR TEST aktiviert und \_ \_ deaktiviert. Während der Scissor-Test aktiviert ist, können nur Pixel, die im Scissor-Feld liegen, durch Zeichnungsbefehle geändert werden. Fensterkoordinaten haben ganzzahlige Werte an den gemeinsamen Ecken von Framepufferpixeln, **sodass glScissor**(0,0,1,1) nur das untere linke Pixel im Fenster geändert werden kann, und **glScissor**(0,0,0,0) lässt änderungen an allen Pixeln im Fenster nicht zu.

Wenn der Scissor-Test deaktiviert ist, sieht es so aus, als ob das Scissor-Feld das gesamte Fenster einschließt.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glScissor** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ SCISSOR \_ BOX

[**glIsEnabled**](glisenabled.md) mit argument GL \_ SCISSOR \_ TEST

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





