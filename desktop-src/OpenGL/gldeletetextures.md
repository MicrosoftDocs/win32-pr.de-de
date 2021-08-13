---
title: glDeleteTextures-Funktion (Gl.h)
description: Die glDeleteTextures-Funktion löscht benannte Texturen.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- glDeleteTextures-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408019d3bfe226c9e7ecdc2ea00182a0b11c78fa64a0210be658ded4556850cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617045"
---
# <a name="gldeletetextures-function"></a>glDeleteTextures-Funktion

Die **glDeleteTextures-Funktion** löscht benannte Texturen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der zu löschenden Texturen.

</dd> <dt>

*Texturen* 
</dt> <dd>

Ein Array von Texturen, die gelöscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *n* war ein negativer Wert.<br/>                                                                                                  |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glDeleteTextures-Funktion** löscht *n Texturen,* die von den Elementen der Arraytexturen *benannt werden.* Nachdem eine Textur gelöscht wurde, hat sie keinen Inhalt oder keine Dimensionalität, und ihr Name kann wiederverwendet werden (z.B. **durch glGenTextures**). Die **glDeleteTextures-Funktion** ignoriert Nullen und Namen, die nicht vorhandenen Texturen entsprechen.

Wenn eine textur, die derzeit gebunden ist, gelöscht wird, wird die Bindung auf null (die Standardtextur) zurückgesetzt.

Aufrufe von **glDeleteTextures** können nicht in Anzeigelisten enthalten sein.

> [!Note]  
> Die **glDeleteTextures-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

Die folgende Funktion ruft Informationen im Zusammenhang mit **glDeleteTextures ab:**

-   [**glIsTexture**](glistexture.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

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

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





