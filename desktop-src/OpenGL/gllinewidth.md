---
title: glLineWidth-Funktion (Gl.h)
description: Die glLineWidth-Funktion gibt die Breite von rasterisierten Linien an.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad5af24170f47125136e87e055413a576821bf75d3f5f87532d026d0bb2fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492970"
---
# <a name="gllinewidth-function"></a>glLineWidth-Funktion

Die **glLineWidth-Funktion** gibt die Breite von rasterisierten Linien an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*width* 
</dt> <dd>

Die Breite von gerasterten Linien. Der Standardwert ist 1.0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *width* war kleiner als oder gleich 0 (null).<br/>                                                                                    |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glLineWidth-Funktion** gibt die rasterisierte Breite von Linien mit Alias und Antialiasing an. Die Verwendung einer anderen Linienbreite als 1,0 hat unterschiedliche Auswirkungen, je nachdem, ob Zeilen antialiasing aktiviert ist. Das Antialiasing von Linien wird durch Aufrufen von [**glEnable**](glenable.md) und **glDisable** mit dem Argument GL \_ LINE SMOOTH \_ gesteuert.

Wenn das Zeilen-Antialiasing deaktiviert ist, wird die tatsächliche Breite bestimmt, indem die angegebene Breite auf die nächste ganze Zahl gerundet wird. (Wenn die Rundung den Wert 0,0 ergibt, ist dies so, als ob die Linienbreite 1,0 wäre.) Wenn \| ? x \|  =  \| ? y \| , *i* Pixel werden in jeder Spalte ausgefüllt, die gerastert wird, wobei *i* der gerundete Wert der *Breite* ist. Andernfalls werden *i* Pixel in jeder Zeile ausgefüllt, die gerastert wird.

Wenn Antialiasing aktiviert ist, erzeugt die Linienrasterung ein Fragment für jedes Pixelquadrat, das den Bereich innerhalb des Rechtecks überschneidet, wobei die Breite gleich der aktuellen Linienbreite, die Länge gleich der tatsächlichen Länge der Linie und zentriert auf dem mathematischen Liniensegment ist. Der Abdeckungswert für jedes Fragment ist der Fensterkoordinatenbereich der Schnittmenge des rechteckigen Bereichs mit dem entsprechenden Pixelquadrat. Dieser Wert wird gespeichert und im letzten Rasterungsschritt verwendet.

Nicht alle Breiten können unterstützt werden, wenn Zeilen antialiasing aktiviert ist. Wenn eine nicht unterstützte Breite angefordert wird, wird die nächste unterstützte Breite verwendet. Es wird garantiert nur die Breite 1,0 unterstützt. andere hängen von der Implementierung ab. Der Bereich der unterstützten Breiten und der Größenunterschied zwischen unterstützten Breiten innerhalb des Bereichs können durch Aufrufen von **glGet** mit den Argumenten GL LINE WIDTH RANGE und GL LINE WIDTH GRANULARITY abgefragt \_ \_ \_ \_ \_ \_ werden.

Die von **glLineWidth** angegebene Linienbreite wird immer zurückgegeben, wenn GL \_ LINE WIDTH abgefragt \_ wird. Das Klammern und Runden für Alias- und Antialiasinglinien hat keine Auswirkungen auf den angegebenen Wert.

Die Nicht-Antialiased-Linienbreite kann an einen implementierungsabhängigen Höchstwert gebunden werden. Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner als der Höchstwert für gealiaste Zeilen sein, gerundet auf den nächsten ganzzahligen Wert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glLineWidth** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ LINE \_ WIDTH

**glGet** mit argument GL \_ LINE \_ WIDTH \_ RANGE

**glGet** mit Argument GL \_ LINE \_ WIDTH \_ GRANULARITY

[**glIsEnabled**](glisenabled.md) mit dem Argument GL \_ LINE \_ SMOOTH

## <a name="requirements"></a>Anforderungen



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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





