---
title: glGetPixelMapusv-Funktion (Gl.h)
description: Die Funktionen glGetPixelMapfv, glGetPixelMapuiv und glGetPixelMapusv geben die angegebene Pixelzuordnung zurück. | glGetPixelMapusv-Funktion (Gl.h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- glGetPixelMapusv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f879da92c9c31b4f44a7e65d8648f94c94fcfaaa8ab3a9d88a39ffc15bd57e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494130"
---
# <a name="glgetpixelmapusv-function"></a>glGetPixelMapusv-Funktion

Die [**Funktionen glGetPixelMapfv,**](glgetpixelmapfv.md) [**glGetPixelMapuiv**](glgetpixelmapuiv.md)und **glGetPixelMapusv** geben die angegebene Pixelzuordnung zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*map* 
</dt> <dd>

Der Name der zurückzukehrenden Pixelzuordnung. Akzeptierte Werte sind GL PIXEL MAP I TO \_ \_ \_ \_ \_ I, GL \_ PIXEL MAP S TO \_ \_ \_ \_ S, GL PIXEL MAP I \_ TO \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B, GL PIXEL MAP \_ \_ I \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A, GL PIXEL MAP \_ R TO \_ \_ \_ \_ R, GL PIXEL MAP \_ G TO \_ \_ \_ \_ G, GL PIXEL MAP \_ B TO B und GL PIXEL MAP A \_ TO \_ \_ \_ \_ \_ \_ \_ \_ A.

</dd> <dt>

*Werte* 
</dt> <dd>

Gibt den Inhalt der Pixelzuordnung zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *map* war kein akzeptierter Wert.<br/>                                                                                           |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Eine Beschreibung der zulässigen Werte für den  map-Parameter finden Sie unter [**glPixelMap.**](glpixelmap.md) Die **glGetPixelMap-Funktion** gibt in *Werten den* Inhalt der Pixelzuordnung zurück, die in map angegeben *ist.* Verwenden Sie Pixelzuordnungen während der Ausführung von [**glReadPixels,**](glreadpixels.md) [**glDrawPixels,**](gldrawpixels.md) [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)und [**glTexImage2D,**](glteximage2d.md) um Farbindizes, Schablonenindizes, Farbkomponenten und Tiefenkomponenten anderen Werten zu zuordnen.

Ganzzahlwerte ohne Vorzeichen werden, falls angefordert, linear aus der internen festen Darstellung oder Gleitkommadarstellung zugeordnet, damit 1,0 dem größten darstellbaren ganzzahligen Wert und 0,0 null zugeordnet wird. Rückgabewerte für ganze Zahlen ohne Vorzeichen sind nicht definiert, wenn der Zuordnungswert nicht im Bereich \[ von 0,1 \] liegt.

Um die erforderliche Größe der Zuordnung *zu bestimmen,* rufen [**Sie glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) der entsprechenden symbolischen Konstante auf.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der Werte *vorgenommen.*

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glGetPixelMap ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argument GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet mit** Argument GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit dem Argument GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet mit** Argument GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

 

 





