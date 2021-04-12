---
title: glpopclientattrb-Funktion (GL. h)
description: Die Funktionen glpushclientattab und glpopclientatpub speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her. | glpopclientattrb-Funktion (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glpopclientattrb-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353349"
---
# <a name="glpopclientattrib-function"></a>glpopclientattrb-Funktion

Die Funktionen [**glpushclientattab**](glpushclientattrib.md) und **glpopclientatpub** speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                               | Bedeutung                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL- \_ Stapel \_ Überlauf**</dt> </dl> | Die Funktion wurde aufgerufen, während der Client Attribut Stapel voll war.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glpushclientatpub** -Funktion verwendet den mask-Parameter, um zu bestimmen, welche Gruppen von Client Zustandsvariablen im Client Attribut Stapel gespeichert werden. Sie können den bitweisen OR-Operator verwenden, um akzeptierte symbolische Konstanten zum Festlegen von Bits und zum Erstellen einer Maske zusammenzufassen.

Die Funktion " **glpopclientatpub** " stellt die Werte der Client Zustandsvariablen wieder her, die zuletzt mit " **glpushclientatpub**" gespeichert wurden. Nicht zuvor gespeicherte Client Zustandsvariablen bleiben unverändert. Durch das Übertragen von Attributen auf einen vollständigen Client Attribut Stapel oder das Pop von Attributen aus einem leeren Stapel wird ein Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen. Der Client Attribut Stapel ist standardmäßig leer.

Einige OpenGL-Client Zustands Werte können nicht auf dem Client Attribut Stapel gespeichert werden. Beispielsweise können Sie die SELECT-oder Feedback Zustände nicht im Client Attribut Stapel speichern. Die Tiefe des Client Attribut Stapels beträgt mindestens 16.

Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " werden nicht in Anzeigelisten kompiliert, sondern sofort ausgeführt.

Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " können nur die Pixel Speicher Modi per Push und Pop und den Scheitelpunkt Array-Client Status per Push Sie müssen zum überführen von Push-und Pop-Zuständen, die auf dem Server aufbewahrt werden, [**glpushattab**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) verwenden.

> [!Note]  
> Die Funktionen **glpushclientatpub** und **glpopclientatpub** sind nur in OpenGL, Version 1,1 oder höher, verfügbar.

 

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpushclientatpub** und **glpopclientatpub** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Client- \_ attrb- \_ Stapel \_ Tiefe

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. Client Nachweis \_ \_ \_ \_ Tiefe für Client Nachweis

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

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldisableclientstate**](gldisableclientstate.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glenableclientstate**](glenableclientstate.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgeterror**](glgeterror.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpushatpub**](glpushattrib.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





