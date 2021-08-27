---
title: glPopAttrib-Funktion (Gl.h)
description: Popt den Attributstapel.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib-Funktion OpenGL
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
ms.openlocfilehash: 92034154138ab3747ce190c05716e2df0d82ed3f6b26aba38da780873ce03721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081450"
---
# <a name="glpopattrib-function"></a>glPopAttrib-Funktion

Popt den Attributstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Die Funktion wurde aufgerufen, während der Attributstapel leer war.<br/>                                                               |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die [**glPushAttrib-Funktion**](glpushattrib.md) verwendet ein Argument, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attributstapel gespeichert werden sollen. Symbolische Konstanten werden verwendet, um Bits in der Maske zu setzen. Der mask-Parameter wird in der Regel durch **OR** erstellt, indem mehrere dieser Konstanten zusammen verwendet werden. Die spezielle Maske GL ALL ATTRIB BITS kann verwendet werden, \_ um alle \_ \_ stapelbaren Zustände zu speichern.

Die **glPopAttrib-Funktion** stellt die Werte der Zustandsvariablen wieder wieder auf, die mit dem letzten [**glPushAttrib-Befehl gespeichert**](glpushattrib.md) wurden. Die nicht gespeicherten bleiben unverändert.

Es ist ein Fehler, Attribute auf einen vollständigen Stapel zu pushen oder Attribute aus einem leeren Stapel zu popen. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Anfangs ist der Attributstapel leer.

Nicht alle Werte für den OpenGL-Status können im Attributstapel gespeichert werden. Beispielsweise können der Pixelpaket- und Entpackungszustand, der Rendermoduszustand und der Auswahl- und Feedbackzustand nicht gespeichert werden.

Die Tiefe des Attributstapels hängt von der Implementierung ab, muss jedoch mindestens 16 sein.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glPushAttrib**](glpushattrib.md) und **glPopAttrib ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





