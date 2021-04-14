---
title: glistexture-Funktion (GL. h)
description: Die Funktion "glistexture" bestimmt, ob ein Name einer Textur entspricht.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- Funktion "glistexture" OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478711"
---
# <a name="glistexture-function"></a>glistexture-Funktion

Die Funktion " **glistexture** " bestimmt, ob ein Name einer Textur entspricht.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Konsistenz* 
</dt> <dd>

Ein-Wert, der den Namen einer Textur ist.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn der *Textur* Parameter derzeit der Name einer Textur ist, gibt die Funktion " **glistexture** " den Wert "GL true" zurück \_ . Die Funktion " **glistexture** " gibt "GL false" zurück, \_ Wenn *Textur* NULL ist. Außerdem wird "GL false" zurückgegeben, \_ Wenn es sich um einen Wert ungleich 0 (null) handelt, der derzeit nicht der Name einer Textur ist, oder wenn ein Fehler auftritt.

Sie können keine Aufrufe von " **glistexture** " in Anzeigelisten einschließen.

> [!Note]  
> Die Funktion " **glistexture** " ist nur in OpenGL, Version 1,1 oder höher, verfügbar.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgentexturen**](glgentextures.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





