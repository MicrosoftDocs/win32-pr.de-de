---
title: glMatrixMode-Funktion (GL. h)
description: Die glMatrixMode-Funktion gibt an, welche Matrix die aktuelle Matrix ist.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104679"
---
# <a name="glmatrixmode-function"></a>glMatrixMode-Funktion

Die **glMatrixMode** -Funktion gibt an, welche Matrix die aktuelle Matrix ist.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Der Matrix Stapel, der das Ziel für nachfolgende Matrix Vorgänge ist. Der *Mode* -Parameter kann einen von drei Werten annehmen.



| Wert                                                                                                                                                         | Bedeutung                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <dt>**GL \_ Modelview**</dt> </dl>    | Wendet nachfolgende Matrix Vorgänge auf den Modelview-Matrix Stapel an.<br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <dt>**GL- \_ Projektion**</dt> </dl> | Wendet nachfolgende Matrix Vorgänge auf den Projektions Matrix Stapel an.<br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <dt>**GL- \_ Textur**</dt> </dl>          | Wendet nachfolgende Matrix Vorgänge auf den Textur Matrix Stapel an.<br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glMatrixMode** -Funktion legt den aktuellen Matrix Modus fest.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glMatrixMode** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus

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

[**glloadmatrix**](glloadmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





