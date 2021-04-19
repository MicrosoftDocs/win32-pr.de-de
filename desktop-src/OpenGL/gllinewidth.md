---
title: glLineWidth-Funktion (GL. h)
description: Die Funktion "glLineWidth" gibt die Breite von rasterisierten Linien an.
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
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343066"
---
# <a name="gllinewidth-function"></a>glLineWidth-Funktion

Die Funktion " **glLineWidth** " gibt die Breite von rasterisierten Linien an.

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

Die Breite von rasterisierten Linien. Der Standardwert ist 1.0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *Breite* war kleiner als oder gleich 0 (null).<br/>                                                                                    |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glLineWidth** " gibt die gerenderte Breite sowohl von Aliasing-als auch von Antialiasing-Zeilen an. Die Verwendung einer anderen Linienbreite als 1,0 hat unterschiedliche Effekte, je nachdem, ob das linienantialiasing aktiviert ist. Das Antialiasing von Zeilen wird durch Aufrufen von [**glEnable**](glenable.md) und **gldeaktiviert** mit dem Argument GL \_ line \_ Smooth gesteuert.

Wenn das Zeilen-Antialiasing deaktiviert ist, wird die tatsächliche Breite festgelegt, indem die angegebene Breite auf die nächste ganze Zahl gerundet wird. (Wenn die Rundung den Wert 0,0 ergibt, ist Sie so, als ob die Linienstärke 1,0 wäre.) Wenn \| ? x \|  =  \| ? y \| , *i* Pixel werden in jede Spalte eingefügt, die rasterisiert ist, wobei *ich* den gerundeten Wert von *Width* verwende. Andernfalls wird jede Zeile, die gerengt wird, in " *i* Pixel" aufgefüllt.

Wenn Antialiasing aktiviert ist, erzeugt die linienrasterisierung ein Fragment für jedes Pixel Quadrat, das den Bereich überschneidet, der innerhalb des Rechtecks liegt und dessen Breite gleich der aktuellen Linienstärke, der Länge der tatsächlichen Länge der Zeile und der zentriert auf dem mathematischen Liniensegment liegt. Der Abdeckungs Wert für jedes Fragment ist der Fenster Koordinaten Bereich der Schnittmenge des rechteckigen Bereichs mit dem entsprechenden Pixel Quadrat. Dieser Wert wird gespeichert und im abschließenden rasterisierungsschritt verwendet.

Nicht alle breiten können unterstützt werden, wenn das linienantialiasing aktiviert ist. Wenn eine nicht unterstützte Breite angefordert wird, wird die nächste unterstützte Breite verwendet. Es wird sichergestellt, dass nur die Breite 1,0 unterstützt wird. andere sind von der Implementierung abhängig. Der Bereich der unterstützten breiten und der Größenunterschied zwischen unterstützten breiten innerhalb des Bereichs kann durch Aufrufen von **glget** mit den Argumenten GL \_ \_ -Linienbreite \_ und- \_ \_ \_ Granularität der GL-Linie abgefragt werden.

Die durch **glLineWidth** angegebene Linienbreite wird immer zurückgegeben, wenn die GL- \_ Linien \_ Breite abgefragt wird. Das Spannen und Runden von Zeilen mit einem Alias und einem mit einem AntiAlias einhergehenden Zeilen haben keine Auswirkung auf den angegebenen Wert.

Die Linienbreite ohne Antialiasing kann an einen von der Implementierung abhängigen Höchstwert gebunden werden. Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner sein als der Maximalwert für Antialiasing-Zeilen, gerundet auf den nächsten ganzzahligen Wert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glLineWidth** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Linien \_ Breite

**glget** mit Argument GL- \_ Linien \_ Breite \_ Bereich

**glget** mit Argument GL- \_ Linienstärke \_ \_ Granularität

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ line \_ Smooth

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
</dt> </dl>

 

 





