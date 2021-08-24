---
title: glGetTexEnvfv-Funktion (Gl.h)
description: Die Funktionen glGetTexEnvfv und glGetTexEnviv geben Texturumgebungsparameter zurück. | glGetTexEnvfv-Funktion (Gl.h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b294879711662c67f9ab581e89eaadfa620363e1d19e93f7ea686ba7453a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493870"
---
# <a name="glgettexenvfv-function"></a>glGetTexEnvfv-Funktion

Die Funktionen **glGetTexEnvfv** und [**glGetTexEnviv**](glgettexenviv.md) geben Texturumgebungsparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Eine Texturumgebung. Muss GL \_ TEXTURE \_ ENV sein.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name eines Texturumgebungsparameters. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**GL \_ TEXTURE \_ ENV \_ MODE**</dt> </dl>    | Der *parameter-Parameter* gibt den Umgebungsmodus für eine einwertige Textur zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**GL \_ TEXTURE \_ ENV \_ COLOR**</dt> </dl> | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Farbe der Texturumgebung darstellen. Ganzzahlige Werte werden bei Anforderung linear aus der internen Gleitkommadarstellung zugeordnet, sodass 1,0 der positivsten darstellbaren ganzen Zahl und -1,0 der negativsten darstellbaren ganzen Zahl zugeordnet wird.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *pname* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetTexEnv-Funktion** gibt in *params* ausgewählte Werte einer Texturumgebung zurück, die mit [**glTexEnv**](gltexenv-functions.md)angegeben wurde. Der *Zielparameter* gibt eine Texturumgebung an. Derzeit wird nur eine Texturumgebung definiert und unterstützt: GL \_ TEXTURE \_ ENV.

Der *pname-Parameter* benennt einen bestimmten Texturumgebungsparameter.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Parameter* vorgenommen.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





