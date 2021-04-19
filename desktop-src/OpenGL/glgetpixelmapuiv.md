---
title: glgetpixelmapuiv-Funktion (GL. h)
description: Die Funktionen "glgetpixelmapfv", "glgetpixelmapuiv" und "glgetpixelmapusv" geben die angegebene Pixel Map zurück. | glgetpixelmapuiv-Funktion (GL. h)
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- glgetpixelmapuiv-Funktion OpenGL
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
ms.openlocfilehash: 1c017e7601e074c588aa534b6ea90aef79325ed4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366585"
---
# <a name="glgetpixelmapuiv-function"></a>glgetpixelmapuiv-Funktion

Die Funktionen " [**glgetpixelmapfv**](glgetpixelmapfv.md)", " **glgetpixelmapuiv**" und " [**glgetpixelmapusv**](glgetpixelmapusv.md) " geben die angegebene Pixel Map zurück.

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

Der Name der zurück zugebende Pixel Zuordnung. Akzeptierte Werte sind GL \_ Pixel \_ map \_ i \_ to \_ i, GL \_ Pixel \_ map \_ s \_ to \_ s, GL \_ Pixel \_ map \_ i \_ to \_ r, GL \_ Pixel \_ map \_ i \_ to \_ g, GL \_ Pixel \_ map \_ i \_ to \_ b, GL \_ Pixel \_ map \_ i \_ to \_ a, GL \_ Pixel \_ map \_ r \_ to \_ r, GL \_ Pixel \_ map \_ g \_ to \_ G, GL \_ Pixel \_ map \_ b \_ to \_ b und GL \_ Pixel \_ map \_ a \_ to \_ a.

</dd> <dt>

*Werte* 
</dt> <dd>

Gibt den Pixel Karteninhalt zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *map* war kein akzeptierter Wert.<br/>                                                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Eine Beschreibung der zulässigen Werte für den *map* -Parameter finden Sie unter [**glpixelmap**](glpixelmap.md) . Die **glgetpixelmap** -Funktion gibt den Inhalt der in *map* angegebenen Pixel Zuordnung in den *Werten* zurück. Verwenden Sie Pixel Zuordnungen während der Ausführung von [**glread Pixel**](glreadpixels.md), [**gldrawpixels**](gldrawpixels.md), [**glcopypixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)und [**glTexImage2D**](glteximage2d.md) , um Farbindizes, Schablone-Indizes, Farbkomponenten und tiefen Komponenten anderen Werten zuzuordnen.

Ganzzahlige Werte ohne Vorzeichen werden, falls angefordert, linear aus der internen Fixed-oder Gleit Komma Darstellung zugeordnet, sodass 1,0 dem größten darstellbaren ganzzahligen Wert zugeordnet ist und 0,0 0 (null) zugeordnet wird. Die Rückgabe ganzzahliger Werte ohne Vorzeichen sind nicht definiert, wenn der Zuordnungs Wert nicht im Bereich von \[ 0, 1 liegt \] .

Um die erforderliche Größe von *map* zu ermitteln, nennen [**Sie glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der entsprechenden symbolischen Konstante.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Werte* vorgenommen.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glgetpixelmap** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pixel \_ map \_ i \_ to \_ i \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ s \_ to \_ s \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ R \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ G \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ B \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ A \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ r \_ to \_ r \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ g \_ bis \_ g \_ size

**glget** mit Argument GL \_ Pixel \_ map \_ b \_ bis \_ b \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ a \_ to \_ a \_ size

**glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glpixelmap**](glpixelmap.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





