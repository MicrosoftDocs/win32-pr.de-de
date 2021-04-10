---
title: glloadname-Funktion (GL. h)
description: Die Funktion "glloadname" lädt einen Namen in den Namen Stapel.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glloadname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106412"
---
# <a name="glloadname-function"></a>glloadname-Funktion

Die Funktion " **glloadname** " lädt einen Namen in den Namen Stapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Ein Name, der den obersten Wert des Namens Stapels ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde aufgerufen, während der namens Stapel leer war.<br/>                                                                    |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glloadname** " bewirkt, dass *Name* den Wert am Anfang des Namens Stapels ersetzt, der anfänglich leer ist. Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können. Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.

Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ . Aufrufe von **glloadname** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit " **glloadname**" abgerufen:

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

[**glinitnames**](glinitnames.md)
</dt> <dt>

[**glpushname**](glpushname.md)
</dt> <dt>

[**glrendermode**](glrendermode.md)
</dt> <dt>

[**glselectbuffer**](glselectbuffer.md)
</dt> </dl>

 

 





