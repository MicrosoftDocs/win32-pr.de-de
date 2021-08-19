---
title: glPointSize-Funktion (Gl.h)
description: Die glPointSize-Funktion gibt den Eigenschaftenbereich von rasterisierten Punkten an.
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
ms.openlocfilehash: 127618e483a300024201798f7c8728d9ab8c0c0807e6dcac07ba580798a1ea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132821"
---
# <a name="glpointsize-function"></a>glPointSize-Funktion

Die **glPointSize-Funktion** gibt den Eigenschaftenbereich von rasterisierten Punkten an.

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

Der Eigenschaftenbereich von rasterten Punkten. Der Standardwert ist 1.0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *size* war kleiner oder gleich 0 (null).<br/>                                                                                     |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glPointSize-Funktion** gibt den rasterisierten Eigenschaftenbereich von Alias- und Antialiasingpunkten an. Die Verwendung einer anderen Punktgröße als 1,0 hat unterschiedliche Auswirkungen, je nachdem, ob Punkt-Antialiasing aktiviert ist. Das Antialiasing von Punkt wird durch Aufrufen [**von glEnable**](glenable.md) und **glDisable** mit dem Argument GL \_ POINT SMOOTH \_ gesteuert.

Wenn das Antialiasing von Punkten deaktiviert ist, wird die tatsächliche Größe bestimmt, indem die angegebene Größe auf die nächste ganze Zahl gerundet wird. (Wenn die Rundung den Wert 0 ergibt, ist dies so, als ob die Punktgröße 1 wäre.) Wenn die gerundete Größe ungerade ist, wird der Mittelpunkt (*x*,*y*) des Pixelfragments, das den Punkt darstellt, als berechnet.

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

wobei  w-Inskripts Fensterkoordinaten angeben. Alle Pixel, die innerhalb des quadratischen Rasters der abgerundeten Größe liegen, die um (*x*,*y*) zentriert sind, stellen das Fragment dar. Wenn die Größe gleichmäßig ist, ist der Mittelpunkt

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

und die Mittelpunkte des rasterisierten Fragments sind die Halb-Ganzzahl-Fensterkoordinaten innerhalb des Quadrats der abgerundeten Größe, die um (*x*, y )*zentriert ist.* Allen Pixelfragmenten, die beim Rastern eines nicht vorsenden Punkts erzeugt werden, werden die gleichen zugeordneten Daten zugewiesen. die des Scheitelpunkts, der dem Punkt entspricht.

Wenn Antialiasing aktiviert ist, erzeugt die Punktrasterung ein Fragment für jedes Pixel-Quadrat, das den bereich schneidet, der innerhalb des Kreises liegt, deren Partikel gleich der aktuellen Punktgröße ist und an den Punkten zentriert ist (*x*<sub>w</sub> ,*y*<sub>w</sub> ). Der Abdeckungswert für jedes Fragment ist der Fensterkoordinatenbereich der Schnittmenge des kreisförmigen Bereichs mit dem entsprechenden Pixel-Quadrat. Dieser Wert wird gespeichert und im letzten Rasterungsschritt verwendet. Die den einzelnen Fragmenten zugeordneten Daten sind die Daten, die dem punkt zugeordnet sind, der rastert.

Nicht alle Größen werden unterstützt, wenn Das Antialiasing von Punkt aktiviert ist. Wenn eine nicht unterstützte Größe angefordert wird, wird die nächstgelegene unterstützte Größe verwendet. Es wird garantiert, dass nur die Größe 1.0 unterstützt wird. andere hängen von der Implementierung ab. Der Bereich der unterstützten Größen und der Größenunterschied zwischen unterstützten Größen innerhalb des Bereichs können durch Aufrufen von [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit den Argumenten GL POINT SIZE RANGE und \_ GL POINT SIZE \_ \_ \_ \_ \_ GRANULARITY abgefragt werden.

Die von **glPointSize** angegebene Punktgröße wird immer zurückgegeben, wenn GL \_ POINT SIZE \_ abgefragt wird. Das Schließen und Runden von Alias- und Antialiasingpunkten hat keine Auswirkungen auf den angegebenen Wert.

Die Größe von nicht antialiasierten Punkten kann an ein implementierungsabhängiges Maximum geklammert werden. Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner als der Höchstwert für Antialiasingpunkte sein, gerundet auf den nächsten ganzzahligen Wert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPointSize ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ POINT \_ SIZE

**glGet** mit Argument GL \_ POINT \_ SIZE \_ RANGE

**glGet** mit Argument GL \_ POINT \_ SIZE \_ GRANULARITY

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ POINT \_ SMOOTH

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
</dt> </dl>

 

 





