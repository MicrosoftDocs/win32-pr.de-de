---
title: glGetPixelMapuiv-Funktion (Gl.h)
description: Die Funktionen glGetPixelMapfv, glGetPixelMapuiv und glGetPixelMapusv geben die angegebene Pixelzuordnung zurück. | glGetPixelMapuiv-Funktion (Gl.h)
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- glGetPixelMapuiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57a8c8354cea3fe43854824da5d4a139f648d7e0615b425fbf7945da9d69fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012188"
---
# <a name="glgetpixelmapuiv-function"></a>glGetPixelMapuiv-Funktion

Die Funktionen [**glGetPixelMapfv,**](glgetpixelmapfv.md) **glGetPixelMapuiv** und [**glGetPixelMapusv**](glgetpixelmapusv.md) geben die angegebene Pixelzuordnung zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetPixelMapuiv(
   GLenum map,
   GLuint *values
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*map* 
</dt> <dd>

Der Name der zurückzugebende Pixelzuordnung. Zulässige Werte sind GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP S \_ \_ TO \_ \_ \_ S, GL PIXEL MAP I \_ TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ \_ G, GL PIXEL MAP I \_ TO \_ \_ \_ \_ B, GL PIXEL MAP I \_ TO \_ \_ \_ \_ A, GL PIXEL MAP R \_ TO \_ \_ \_ \_ R, GL PIXEL MAP \_ G TO \_ \_ \_ \_ G, GL PIXEL MAP \_ B TO B und GL PIXEL MAP A \_ TO \_ \_ \_ \_ \_ \_ \_ \_ A.

</dd> <dt>

*Werte* 
</dt> <dd>

Gibt den Inhalt der Pixelzuordnung zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *map* war kein akzeptierter Wert.<br/>                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Eine Beschreibung der zulässigen Werte für den *map-Parameter* finden Sie unter [**glPixelMap.**](glpixelmap.md) Die **glGetPixelMap-Funktion** gibt in *-Werten* den Inhalt der in *map* angegebenen Pixelzuordnung zurück. Verwenden Sie Pixelzuordnungen während der Ausführung von [**glReadPixels,**](glreadpixels.md) [**glDrawPixels,**](gldrawpixels.md) [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)und [**glTexImage2D,**](glteximage2d.md) um Farbindizes, Schablonenindizes, Farbkomponenten und Tiefenkomponenten anderen Werten zuzuordnen.

Ganzzahlige Werte ohne Vorzeichen werden, falls angefordert, linear aus der internen festen oder Gleitkommadarstellung zugeordnet, sodass 1,0 dem größten darstellbaren ganzzahligen Wert und 0,0 null zugeordnet wird. Rückgabewerte für ganze Zahlen ohne Vorzeichen sind nicht definiert, wenn der Zuordnungswert nicht im Bereich \[ von 0,1 \] lag.

Um die erforderliche Größe der *Zuordnung* zu bestimmen, rufen [**Sie glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der entsprechenden symbolischen Konstante auf.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt der *Werte* vorgenommen.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glGetPixelMap** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





