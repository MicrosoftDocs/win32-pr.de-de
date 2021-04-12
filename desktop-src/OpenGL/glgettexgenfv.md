---
title: glgettexgenfv-Funktion (GL. h)
description: Die Funktionen "glgettexgendv", "glgettexgenfv" und "glgettexgeniv" geben Texturkoordinaten Generierungs Parameter zurück. | glgettexgenfv-Funktion (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- glgettexgenfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352849"
---
# <a name="glgettexgenfv-function"></a>glgettexgenfv-Funktion

Die Funktionen " [**glgettexgendv**](glgettexgendv.md)", " **glgettexgenfv**" und " [**glgettexgeniv**](glgettexgeniv.md) " geben Texturkoordinaten Generierungs Parameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Koord* 
</dt> <dd>

Eine Textur Koordinate. Muss "GL \_ S", "GL \_ T", "GL \_ R" oder "GL \_ Q" lauten.

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name der Werte, die zurückgegeben werden sollen. Muss entweder der GL- \_ Textur \_ gen- \_ Modus oder der Name einer der Gleichungen der Textur Generierungs Ebene sein: GL- \_ Objekt \_ Ebene oder GL- \_ Augen \_ Ebene. Diese Werte lauten wie folgt:



| Wert                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**GL- \_ Textur \_ gen- \_ Modus**</dt> </dl> | Der Parameter *para* meters gibt die einwertige Textur Generierungs Funktion zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**GL- \_ Objekt \_ Ebene**</dt> </dl>              | Der Parameter *para* meters gibt die Gleichung der vierstufigen Gleichung zurück, die die Generierung von Objekt linearen Koordinaten angeben. Ganzzahlige Werte werden, wenn angefordert, direkt aus der internen Gleit Komma Darstellung zugeordnet.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**GL- \_ Augen \_ Ebene**</dt> </dl>                       | Der Parameter *para* meters gibt die Gleichung der vierstufigen Gleichung zurück, die die Generierung von Augen linearen Koordinaten angeben. Ganzzahlige Werte werden, wenn angefordert, direkt aus der internen Gleit Komma Darstellung zugeordnet. Die zurückgegebenen Werte werden in den Augen Koordinaten verwaltet. Sie sind nicht mit den Werten identisch, die mithilfe von [**gltexgen**](gltexgen-functions.md)angegeben wurden, es sei denn, die Modelview-Matrix wurde zum Zeitpunkt des Aufrufs von **gltexgen** identifiziert.<br/> |



 

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
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *coord* oder *PName* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glgettexgen** -Funktion gibt in *Parameter ausgewählte Parameter* einer Texturkoordinaten Generierungs Funktion zurück, die Sie mit **gltexgen** angegeben haben. Der *coord* -Parameter benennt eine der (*s*-, *t*-, *r*-, *q*)-Texturkoordinaten, indem er die symbolische Konstante GL \_ s, GL \_ t, GL \_ r oder GL \_ q verwendet.

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

[**gltexgen**](gltexgen-functions.md)
</dt> </dl>

 

 





