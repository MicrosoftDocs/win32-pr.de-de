---
title: glgentexturen-Funktion (GL. h)
description: Die Funktion "glgentexturen" generiert Textur Namen.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glgentexturen-Funktion OpenGL
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
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957080"
---
# <a name="glgentextures-function"></a>glgentexturen-Funktion

Die Funktion " **glgentexturen** " generiert Textur Namen.

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

Die Anzahl der zu generierenden Textur Namen.

</dd> <dt>

*Textur* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Arrays, in dem die generierten Textur Namen gespeichert werden.

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

Die **glgentexturen** -Funktion gibt *n* Textur Namen im *Texturen* -Parameter zurück. Bei den Textur Namen handelt es sich nicht unbedingt um einen zusammenhängenden Satz von Ganzzahlen, aber keine der zurückgegebenen Namen können unmittelbar vor dem Aufrufen der Funktion " **glgentexturen** " verwendet werden. Die generierten Texturen übernehmen die Dimensionalität des Textur Ziels, an das Sie zuerst mit der [**glBindTexture**](glbindtexture.md) -Funktion gebunden werden. Von **glgentexturen** zurückgegebene Textur Namen werden nicht durch nachfolgende Aufrufe von **glgentexturen** zurückgegeben, es sei denn, Sie werden zuerst durch Aufrufen von [**gldeletetexturen**](gldeletetextures.md)gelöscht.

Sie können " **glgentexturen** " nicht in Anzeigelisten einschließen.

> [!Note]  
> Die **glgentexturen** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glgentexturen** ab:

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**gldeletetexturen**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glistexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





