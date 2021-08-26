---
title: glAreTexturesResident-Funktion (Gl.h)
description: Die glAreTexturesResident-Funktion bestimmt, ob angegebene Texturobjekte im Texturspeicher enthalten sind.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c503cac59bbec912c535120161d27991118dab818a185c1f39d8f48cb2a5939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082240"
---
# <a name="glaretexturesresident-function"></a>glAreTexturesResident-Funktion

Die **glAreTexturesResident-Funktion** bestimmt, ob angegebene Texturobjekte im Texturspeicher enthalten sind.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der zu abfragenden Texturen.

</dd> <dt>

*Texturen* 
</dt> <dd>

Die Adresse eines Arrays, das die Namen der abgefragten Texturen enthält.

</dd> <dt>

*Residenzen* 
</dt> <dd>

Die Adresse eines Arrays, in dem der Texturstatus zurückgegeben wird. Der Status einer Textur, die  von einem Texturelement benannt wird, wird im entsprechenden Element von *Leiste zurückgegeben.*

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *n* war ein negativer Wert, ein Element in *Texturen* war 0 (null), oder ein Element in *Texturen* enthält keinen Texturbezeichner.<br/> |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/>     |



## <a name="remarks"></a>Hinweise

Auf Computern mit einer begrenzten Menge an Texturspeicher richtet OpenGL einen Arbeitssatz von Texturen ein, die sich im Texturspeicher befinden. Diese Texturen können viel effizienter an ein Texturziel gebunden werden als Texturen, die nicht resident sind.

Die **funktion glAreTexturesResident** fragt den Texturstatus der *n Texturen* ab, die von den Elementen der *Texturen benannt werden.* Wenn alle benannten Texturen resident sind, **gibt glAreTexturesResident** GL TRUE zurück, und der Inhalt der 30-0-Texturen \_ ist unerkannt.  Wenn eine der benannten Texturen nicht resident ist, gibt **glAreTexturesResident** GL FALSE zurück, und der detaillierte Status wird in den n Elementen von \_ *n* von *2 zurückgegeben.*

Wenn ein Element von *Heiterungen* GL TRUE ist, wird die Textur, die durch das entsprechende Element von Texturen benannt wird, \_ im Texturspeicher gespeichert. 

Rufen Sie zum Abfragen des Status einer einzelnen gebundenen  Textur [**glGetTexParameter**](glgettexparameter.md) mit dem Zielparameter auf, der auf die Zieltextur festgelegt ist, an die das Ziel gebunden ist, und legen Sie den *pname-Parameter* auf GL \_ TEXTURE RESIDENT \_ fest. Sie müssen diese Methode verwenden, um den residenten Status einer Standardtextur abfragt.

**GlAreTexturesResident** kann nicht in Anzeigelisten enthalten sein.

Die **glAreTexturesResident-Funktion** gibt den Residencystatus der Texturen zum Zeitpunkt des Aufrufs zurück. Sie garantiert nicht, dass die Texturen zu einem anderen Zeitpunkt erhalten bleiben.

Wenn sich Texturen im virtuellen Speicher befinden (es ist kein Texturspeicher verfügbar), werden sie als immer resident betrachtet.

> [!Note]  
> Die **glAreTexturesResident-Funktion** ist nur in OpenGL Version 1.1 oder höher verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





