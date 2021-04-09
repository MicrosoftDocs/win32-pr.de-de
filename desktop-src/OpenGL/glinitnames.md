---
title: glinitnames-Funktion (GL. h)
description: Die Funktion "glinitnames" initialisiert den namens Stapel.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glinitnames-Funktion OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102943"
---
# <a name="glinitnames-function"></a>glinitnames-Funktion

Die Funktion " **glinitnames** " initialisiert den namens Stapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glinitnames** " bewirkt, dass der Namen Stapel mit seinem standardmäßigen leeren Zustand initialisiert wird. Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können. Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.

Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ . Aufrufe von **glinitnames** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glinitnames** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"

**glget** mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe

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

[**glloadname**](glloadname.md)
</dt> <dt>

[**glpushname**](glpushname.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> <dt>

[**glselectbuffer**](glselectbuffer.md)
</dt> </dl>

 

 





