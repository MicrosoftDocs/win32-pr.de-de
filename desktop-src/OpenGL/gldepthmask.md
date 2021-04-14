---
title: gldepthmask-Funktion (GL. h)
description: Die Funktion "gldepthmask" aktiviert oder deaktiviert das Schreiben in den tiefen Puffer.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- gldepthmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391991"
---
# <a name="gldepthmask-function"></a>gldepthmask-Funktion

Die Funktion " **gldepthmask** " aktiviert oder deaktiviert das Schreiben in den tiefen Puffer.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flag* 
</dt> <dd>

Gibt an, ob der tiefen Puffer zum Schreiben aktiviert ist. Wenn *Flag* 0 (null) ist, ist das Schreiben von tiefen Puffern deaktiviert. Andernfalls ist es aktiviert. Zunächst ist der tiefen Puffer Schreibvorgang aktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die folgende Funktion Ruft Informationen im Zusammenhang mit " **gldepthmask**" ab:

**glget** mit Argument GL- \_ tiefen \_ schreibfrage

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

[**glcolormask**](glcolormask.md)
</dt> <dt>

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**gldepthrange**](gldepthrange.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glindexmask**](glindexmask.md)
</dt> <dt>

[**glstencilmask**](glstencilmask.md)
</dt> </dl>

 

 





