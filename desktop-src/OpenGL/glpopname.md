---
title: glpopname-Funktion (GL. h)
description: Die Funktionen "glpushname" und "glpopname" schieben den namens Stapel per Push und Pop. | glpopname-Funktion (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glpopname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355767"
---
# <a name="glpopname-function"></a>glpopname-Funktion

Die Funktionen " [**glpushname**](glpushname.md) " und " **glpopname** " schieben den namens Stapel per Push und Pop.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL. \_ Stapel \_ Unterlauf**</dt> </dl>   | Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel nur eine einzelne Matrix enthielt.<br/>                                     |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die [**glpushname**](glpushname.md) -Funktion bewirkt, dass der Name auf dem namens Stapel abgelegt wird, der anfänglich leer ist. Die Funktion " **glpopname** " holt einen Namen vom oberen Rand des Stapels ab. Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können. Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.

Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ . Aufrufe von [**glpushname**](glpushname.md) oder **glpopname** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glpushname**](glpushname.md) und **glpopname** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe

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

[**glinitnames**](glinitnames.md)
</dt> <dt>

[**glloadname**](glloadname.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> <dt>

[**glselectbuffer**](glselectbuffer.md)
</dt> </dl>

 

 





