---
title: glGenTextures-Funktion (Gl.h)
description: Die glGenTextures-Funktion generiert Texturnamen.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glGenTextures-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28275bef054b26c2145ab9779ec776297ac7838d0313769123fb1be904a3bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625230"
---
# <a name="glgentextures-function"></a>glGenTextures-Funktion

Die **glGenTextures-Funktion** generiert Texturnamen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der zu generierenden Texturnamen.

</dd> <dt>

*Texturen* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Arrays, in dem die generierten Texturnamen gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *n* war ein negativer Wert.<br/>                                                                                                  |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGenTextures-Funktion** gibt *n* Texturnamen im *Texturenparameter zurück.* Die Texturnamen sind nicht unbedingt ein zusammenhängender Satz von ganzen Zahlen, aber keiner der zurückgegebenen Namen kann unmittelbar vor dem Aufruf der **glGenTextures-Funktion** verwendet worden sein. Die generierten Texturen setzen die Dimensionalität des Texturziels voraus, an das sie zuerst mit der [**glBindTexture-Funktion**](glbindtexture.md) gebunden werden. Texturnamen, die von **glGenTextures** zurückgegeben werden, werden nicht durch nachfolgende Aufrufe von **glGenTextures** zurückgegeben, es sei denn, sie werden zuerst durch Aufrufen von [**glDeleteTextures**](gldeletetextures.md)gelöscht.

Sie können **glGenTextures** nicht in Anzeigelisten einschließen.

> [!Note]  
> Die **glGenTextures-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die folgende Funktion ruft Informationen im Zusammenhang mit **glGenTextures ab:**

-   [**glIsTexture**](glistexture.md)

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

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





