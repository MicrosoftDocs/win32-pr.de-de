---
title: glgettexparameterfv-Funktion (GL. h)
description: Die Funktionen "glgettexparameterfv" und "glgettexparameteriv" geben Textur Parameterwerte zurück. | glgettexparameterfv-Funktion (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- glgettexparameterfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353689"
---
# <a name="glgettexparameterfv-function"></a>glgettexparameterfv-Funktion

Die Funktionen " **glgettexparameterfv** " und " [**glgettexparameteriv**](glgettexparameteriv.md) " geben Textur Parameterwerte zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Der symbolische Name der Ziel Textur. GL \_ Texture \_ 1D und GL \_ Texture \_ 2D werden akzeptiert.

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name eines Textur Parameters. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL- \_ Textur- \_ mag- \_ Filter**</dt> </dl>       | Gibt den einwertigen Textur Vergrößerungs Filter zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL- \_ Textur- \_ Min- \_ Filter**</dt> </dl>       | Gibt den einwertigen Textur Minimierung-Filter zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL- \_ Textur Umbruch \_ \_ S**</dt> </dl>                   | Gibt die einwertige Wrapping Funktion für Texturkoordinaten *s* zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL- \_ Textur Umbruch \_ \_ T**</dt> </dl>                   | Gibt die einwertige Wrapping Funktion für die Textur Koordinate *t* zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**Rahmenfarbe des GL- \_ Textur Rahmens \_ \_**</dt> </dl> | Gibt vier ganzzahlige oder Gleit Komma Zahlen zurück, die die RGBA-Farbe des Textur Rahmens bilden. Gleit Komma Werte werden im Bereich \[ 0, 1 zurückgegeben \] . Ganzzahlige Werte werden als lineare Zuordnung der internen Gleit Komma Darstellung zurückgegeben, sodass 1,0 der positivsten darstellbaren Ganzzahl und-1,0 der negativsten darstellbaren Ganzzahl zugeordnet wird.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**GL- \_ Textur \_ Priorität**</dt> </dl>              | Gibt die Residenz Priorität der Ziel Textur zurück (oder die an Sie gebundene benannte Textur). Der Anfangswert ist 1. Siehe [**glpriorizetexturen**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**GL- \_ Textur \_ residente**</dt> </dl>              | Gibt den Wohnsitz Status der Ziel Textur zurück. Wenn der Wert, der in Parametern zurückgegeben wird \_ , GL true ist, ist die Textur im Texturspeicher ansässig. Siehe [**glaretexturesresidente**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die Textur Parameter zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* oder der *Name* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgettexparameter** " *gibt in Parameter* den Wert oder die Werte des als " *PName*" angegebenen Textur Parameters zurück. Der *target* -Parameter definiert die Ziel Textur (GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D), um eindimensionale oder zweidimensionale Texturierung anzugeben. Der *PName* -Parameter akzeptiert dieselben Symbole wie [**gltexparameter**](gltexparameter-functions.md)mit denselben Interpretationen.

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

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





