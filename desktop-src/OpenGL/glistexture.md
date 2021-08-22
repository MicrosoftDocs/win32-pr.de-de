---
title: glIsTexture-Funktion (Gl.h)
description: Die glIsTexture-Funktion bestimmt, ob ein Name einer Textur entspricht.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture-Funktion OpenGL
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
ms.openlocfilehash: 7db28b6892d5aa0e9eaf98aec50b02ad102db8ba549474c673c6c0d918d799d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493350"
---
# <a name="glistexture-function"></a>glIsTexture-Funktion

Die **glIsTexture-Funktion** bestimmt, ob ein Name einer Textur entspricht.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Textur* 
</dt> <dd>

Ein -Wert, der dem Namen einer Textur entspricht.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Wenn der *Texturparameter* derzeit der Name einer Textur ist, gibt die **glIsTexture-Funktion** GL \_ TRUE zurück. Die **glIsTexture-Funktion** gibt GL \_ FALSE zurück, wenn die *Textur* 0 (null) ist. Außerdem wird GL FALSE zurückgegeben, wenn es sich um \_ einen Wert ungleich 0 (null) handelt, der derzeit nicht der Name einer Textur ist, oder wenn ein Fehler auftritt.

Aufrufe von **glIsTexture** können nicht in Anzeigelisten eingeschlossen werden.

> [!Note]  
> Die **glIsTexture-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





