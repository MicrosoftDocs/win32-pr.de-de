---
title: glPointSize-Funktion (GL. h)
description: Die Funktion "glPointSize" gibt den Durchmesser der rasterisierten Punkte an.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339987"
---
# <a name="glpointsize-function"></a>glPointSize-Funktion

Die Funktion " **glPointSize** " gibt den Durchmesser der rasterisierten Punkte an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*size* 
</dt> <dd>

Der Durchmesser der rasterisierten Punkte. Der Standardwert ist 1.0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | die *Größe* war kleiner als oder gleich 0 (null).<br/>                                                                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glPointSize** " gibt den rasterisierten Durchmesser von Aliasing-und Antialiasing-Punkten an. Die Verwendung einer anderen Punktgröße als 1,0 hat unterschiedliche Auswirkungen, abhängig davon, ob das Punkt-Antialiasing aktiviert ist. Das Antialiasing von Punkten wird durch Aufrufen von [**glEnable und glEnable**](glenable.md) mit dem Argument GL  \_ Point Smooth gesteuert \_ .

Wenn das Punkt-Antialiasing deaktiviert ist, wird die tatsächliche Größe festgelegt, indem die angegebene Größe auf die nächste ganze Zahl gerundet wird. (Wenn die Rundung den Wert 0 (null) ergibt, ist Sie so, als ob die Punktgröße 1 ist.) Wenn die gerundete Größe ungerade ist, wird der Mittelpunkt (*x*,*y*) des Pixel Fragments, das den Punkt darstellt, als

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

wobei *w* -Index Fenster Fenster Koordinaten angeben. Alle Pixel, die innerhalb des quadratischen Rasters der gerundeten Größe liegen, die auf (*x*,*y*) zentriert ist, bilden das Fragment. Wenn die Größe gerade ist, ist der Mittelpunkt

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

und die Kreis zentrierte Fragmente sind die halbzahligen Fenster Koordinaten innerhalb des Quadrats der gerundeten Größe, die auf (*x*,*y*) zentriert ist. Allen Pixel Fragmenten, die bei der rasterisierung eines nicht-Antialiasing-Punkts erstellt werden, werden dieselben zugeordneten Daten zugewiesen. die des Scheitel Punkts, der dem Punkt entspricht.

Wenn Antialiasing aktiviert ist, erzeugt die Punkt-rasterisierung ein Fragment für jedes Pixel Quadrat, das den Bereich überschneidet, der sich innerhalb des Kreises befindet und einen Durchmesser gleich der aktuellen Punktgröße aufweist und sich an den Punkten (*x*<sub>w</sub> ,*y*<sub>w</sub> ) befindet. Der Abdeckungs Wert für jedes Fragment ist der Fenster Koordinaten Bereich der Schnittmenge des kreisförmigen Bereichs mit dem entsprechenden Pixel Quadrat. Dieser Wert wird gespeichert und im abschließenden rasterisierungsschritt verwendet. Die den einzelnen Fragmenten zugeordneten Daten sind die Daten, die dem zu ragenden Punkt zugeordnet sind.

Nicht alle Größen werden unterstützt, wenn das Punkt-Antialiasing aktiviert ist. Wenn eine nicht unterstützte Größe angefordert wird, wird die nächstgelegene unterstützte Größe verwendet. Es wird garantiert, dass nur die Größe 1,0 unterstützt wird. andere sind von der Implementierung abhängig. Der Bereich der unterstützten Größen und der Größenunterschied zwischen unterstützten Größen innerhalb des Bereichs kann durch Aufrufen von [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit den Argumenten GL \_ \_ -Punktgröße \_ und- \_ Granularität der GL- \_ Punktgröße \_ abgefragt werden.

Die durch **glPointSize** angegebene Punktgröße wird immer zurückgegeben, wenn die GL- \_ Punkt \_ Größe abgefragt wird. Das Spannen und Runden von Aliasing-und Antialiasing-Punkten hat keine Auswirkung auf den angegebenen Wert.

Die Größe des nicht-Antialiasing-Werts kann an einen von der Implementierung abhängigen maximalen Wert gebunden werden. Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner sein als der Maximalwert für Antialiasing Punkte, gerundet auf den nächsten ganzzahligen Wert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glPointSize** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Punkt \_ Größe

**glget** mit Argument-GL- \_ Punkt \_ Größen \_ Bereich

**glget** mit der Granularität der GL- \_ Punktgröße des Arguments \_ \_

[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Point \_ Smooth

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

 

 





