---
title: glgettexenviv-Funktion (GL. h)
description: Die Funktionen "glgettexgetvfv" und "glgettexenviv" geben Textur Umgebungsparameter zurück. | glgettexenviv-Funktion (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- glgettexenviv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354311"
---
# <a name="glgettexenviv-function"></a>glgettexenviv-Funktion

Die Funktionen " [**glgettexgetvfv**](glgettexenvfv.md) " und " **glgettexenviv** " geben Textur Umgebungsparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Eine Textur Umgebung. Muss "GL \_ Texture" sein \_ .

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name eines Textur Umgebungs Parameters. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**GL- \_ Textur \_ env- \_ Modus**</dt> </dl>    | Der Parameter *para* meters gibt den einwertigen Textur Umgebungs Modus zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**GL- \_ Textur Gesamt \_ \_ Farbe**</dt> </dl> | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Farbe der Textur Umgebung sind. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 der positivsten darstellbaren Ganzzahl zugeordnet ist und-1,0 der negativsten darstellbaren Ganzzahl entspricht.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *target* oder *PName* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glgettexenv** -Funktion gibt *in Parameter* ausgewählte Werte einer Textur Umgebung zurück, die mit [**gltexenv**](gltexenv-functions.md)angegeben wurde. Der *Ziel* Parameter gibt eine Textur Umgebung an. Zurzeit wird nur eine Textur Umgebung definiert und unterstützt: GL Texture-Version \_ \_ .

Der *PName* -Parameter benennt einen bestimmten Textur Umgebungsparameter.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.

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

[**gltexd**](gltexenv-functions.md)
</dt> </dl>

 

 





