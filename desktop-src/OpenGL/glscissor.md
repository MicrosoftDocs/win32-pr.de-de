---
title: glscissor-Funktion (GL. h)
description: Die Funktion "glscissor" definiert das Feld "Scheren".
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glscissor-Funktion OpenGL
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
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479131"
---
# <a name="glscissor-function"></a>glscissor-Funktion

Die Funktion " **glscissor** " definiert das Feld "Scheren".

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

Die x-Koordinate (vertikale Achse) für die untere linke Ecke des Scheren Felds.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Koordinate (horizontale Achse) für die untere linke Ecke des Scheren Felds. In kombinieren Sie x und y in der unteren linken Ecke des Scheren Felds. Anfänglich (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Scheren Felds.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Scheren Felds. Wenn ein OpenGL-Kontext zum *ersten Mal* an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | Die *Breite* oder *Höhe* war negativ.<br/>                                                                                   |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glscissor** " definiert ein Rechteck, das als "Scheren"-Feld bezeichnet wird, in Fenster Koordinaten. Die ersten beiden Parameter *x* und *y* geben die untere linke Ecke des Felds an. Die *Width* -und *height* -Parameter geben die Breite und Höhe des Felds an.

Der Scheren-Test wird mit " [**glEnable**](glenable.md) " und " **gldeaktivieren** " mit dem Argument "GL \_ Scheren Test" aktiviert und deaktiviert \_ . Während der Scheren-Test aktiviert ist, können nur Pixel, die im Feld Scheren liegen, durch Zeichnen von Befehlen geändert werden. Fenster Koordinaten verfügen über ganzzahlige Werte in den freigegebenen Ecken von Frame Puffer Pixel, sodass mit **glscissor**(0, 0, 1, 1) nur das untere linke Pixel im Fenster geändert werden kann, und **glscissor**(0, 0, 0, 0) lässt Änderungen an allen Pixeln im Fenster nicht zu.

Wenn der Scheren-Test deaktiviert ist, ist es so, als ob das Feld Scheren das gesamte Fenster enthält.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glscissor** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Scissor \_ Box

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Scissor \_ Test

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





