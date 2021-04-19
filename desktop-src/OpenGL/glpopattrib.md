---
title: glpopattrb-Funktion (GL. h)
description: Springt den Attribut Stapel.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glpopattrb-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338345"
---
# <a name="glpopattrib-function"></a>glpopattrb-Funktion

Springt den Attribut Stapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL. \_ Stapel \_ Unterlauf**</dt> </dl>   | Die Funktion wurde aufgerufen, während der Attribut Stapel leer war.<br/>                                                               |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " [**glpushatpub**](glpushattrib.md) " erfordert ein Argument, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attribut Stapel gespeichert werden sollen. Symbolische Konstanten werden verwendet, um Bits in der Maske festzulegen. Der mask-Parameter wird in der Regel von erstellt, **oder** es werden mehrere dieser Konstanten erstellt. Die besondere Maske GL \_ alle \_ atzb- \_ Bits können zum Speichern aller Stackable-Zustände verwendet werden.

Die Funktion " **glpopatpub** " stellt die Werte der Zustandsvariablen wieder her, die mit dem letzten Befehl " [**glpushatpub**](glpushattrib.md) " gespeichert wurden. Die nicht gespeicherten Änderungen bleiben unverändert.

Es ist ein Fehler, Attribute auf einen vollständigen Stapel zu übersetzen oder Attribute aus einem leeren Stapel zu Pop. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Der Attribut Stapel ist zunächst leer.

Nicht alle Werte für den OpenGL-Zustand können im Attribut Stapel gespeichert werden. Beispielsweise können das Pixel Paket und der Debugzustand, der rendermoduszustand und der Status "Select" und "Feedback" nicht gespeichert werden.

Die Tiefe des Attribut Stapels hängt von der Implementierung ab, muss jedoch mindestens 16 sein.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glpushatpub**](glpushattrib.md) und **glpopatpub** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ Stapel \_ Tiefe des Argument-GL

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ maximalen \_ attrb- \_ Stapel \_ Tiefe des Arguments

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

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetclipplane**](glgetclipplane.md)
</dt> <dt>

[**glgeterror**](glgeterror.md)
</dt> <dt>

[**glgetlight**](glgetlight.md)
</dt> <dt>

[**glgetmap**](glgetmap.md)
</dt> <dt>

[**glgetmaterial**](glgetmaterial.md)
</dt> <dt>

[**glgetpixelmap**](glgetpixelmap.md)
</dt> <dt>

[**glgetpolygonstippel**](glgetpolygonstipple.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glgettex-v**](glgettexenv.md)
</dt> <dt>

[**glgettexgen**](glgettexgen.md)
</dt> <dt>

[**glgetteximage**](glgetteximage.md)
</dt> <dt>

[**glgettexlevelparameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





