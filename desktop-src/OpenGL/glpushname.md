---
title: glpushname-Funktion (GL. h)
description: Die Funktionen "glpushname" und "glpopname" schieben den namens Stapel per Push und Pop. | glpushname-Funktion (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glpushname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371856"
---
# <a name="glpushname-function"></a>glpushname-Funktion

Die Funktionen " **glpushname** " und " [**glpopname**](glpopname.md) " schieben den namens Stapel per Push und Pop.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Ein Name, der auf den Namen Stapel verschoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL- \_ Stapel \_ Überlauf**</dt> </dl>    | Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel voll war.<br/>                                                           |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glpushname** -Funktion bewirkt, dass der Name auf dem namens Stapel abgelegt wird, der anfänglich leer ist. Die Funktion " [**glpopname**](glpopname.md) " holt einen Namen vom oberen Rand des Stapels ab. Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können. Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.

Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ . Aufrufe von **glpushname** oder [**glpopname**](glpopname.md) , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpushname** und [**glpopname**](glpopname.md)ab:

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

 

 





