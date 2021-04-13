---
title: gldeletetexturen-Funktion (GL. h)
description: Die Funktion "gldeletetexturen" löscht benannte Texturen.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- gldeletetexturen-Funktion OpenGL
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
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475675"
---
# <a name="gldeletetextures-function"></a>gldeletetexturen-Funktion

Die Funktion " **gldeletetexturen** " löscht benannte Texturen.

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

*Textur* 
</dt> <dd>

Ein Array von Texturen, die gelöscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *n* war ein negativer Wert.<br/>                                                                                                  |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gldeletetexturen** -Funktion löscht *n* Texturen, die von den Elementen der Array *Texturen* benannt werden. Nachdem eine Textur gelöscht wurde, weist Sie keinen Inhalt oder keine Dimensionalität auf, und der Name ist für die Wiederverwendung frei (z. b. von **glgentexturen**). Die Funktion " **gldeletetexturen** " ignoriert Nullen und Namen, die nicht vorhandenen Texturen entsprechen.

Wenn eine Textur, die gerade gebunden ist, gelöscht wird, wird die Bindung auf NULL (die Standard Textur) zurückgesetzt.

Sie können keine Aufrufe von **gldeletetexturen** in Anzeigelisten einschließen.

> [!Note]  
> Die **gldeletetexturen** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die folgende Funktion Ruft Informationen im Zusammenhang mit **gldeletetexturen** ab:

-   [**glistexture**](glistexture.md)

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

[**glaretexturesresidente**](glaretexturesresident.md)
</dt> <dt>

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

[**glistexture**](glistexture.md)
</dt> <dt>

[**glpriorizetexturen**](glprioritizetextures.md)
</dt> <dt>

[**gltexgen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





