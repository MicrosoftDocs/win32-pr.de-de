---
title: glGetTexParameterfv-Funktion (Gl.h)
description: Die Funktionen glGetTexParameterfv und glGetTexParameteriv geben Texturparameterwerte zurück. | glGetTexParameterfv-Funktion (Gl.h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- glGetTexParameterfv-Funktion OpenGL
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
ms.openlocfilehash: 7925ae070a3e35f6c9b3a9ba65ff506f775b77e625dc852b49cc305c76003428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359710"
---
# <a name="glgettexparameterfv-function"></a>glGetTexParameterfv-Funktion

Die **Funktionen glGetTexParameterfv** und [**glGetTexParameteriv**](glgettexparameteriv.md) geben Texturparameterwerte zurück.

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

Der symbolische Name der Zieltextur. GL \_ TEXTURE \_ 1D und GL \_ TEXTURE \_ 2D werden akzeptiert.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name eines Texturparameters. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MAG \_ FILTER**</dt> </dl>       | Gibt den einwertigen Texturvergrößerungsfilter zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MIN \_ FILTER**</dt> </dl>       | Gibt den einwertigen Texturvergrößerungsfilter zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>                   | Gibt die einwertige Umbruchfunktion für Texturkoordinaten *zurück,* eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Gibt die einwertige Umbruchfunktion für die Texturkoordinate *t* zurück, eine symbolische Konstante.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**GL \_ TEXTURE \_ BORDER \_ COLOR**</dt> </dl> | Gibt vier ganze Zahlen oder Gleitkommazahlen zurück, die die RGBA-Farbe des Texturgrenzwerts umfassen. Gleitkommawerte werden im Bereich \[ 0,1 \] zurückgegeben. Ganzzahlige Werte werden als lineare Zuordnung der internen Gleitkommadarstellung zurückgegeben, damit 1,0 der positivsten darstellbaren ganzen Zahl und -1,0 der negativsten darstellbaren ganzen Zahl zuordnen.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**GL \_ \_ TEXTURPRIORITÄT**</dt> </dl>              | Gibt die Priorität der Priorität der Zieltextur (oder der benannten Textur, die an sie gebunden ist) zurück. Der Anfangswert ist 1. Siehe [**glPrioritizeTextures.**](glprioritizetextures.md)<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**GL \_ TEXTURE \_ RESIDENT**</dt> </dl>              | Gibt den Status der Zieltextur zurück. Wenn der in params zurückgegebene Wert GL \_ TRUE ist, befindet sich die Textur im Texturspeicher. Siehe [**glAreTexturesResident.**](glaretexturesresident.md)<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die Texturparameter zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *name* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetTexParameter-Funktion** gibt in *Parametern* den Wert oder die Werte des Texturparameters zurück, der als *pname angegeben ist.* Der *Zielparameter* definiert die Zieltextur , entweder GL \_ TEXTURE 1D oder GL TEXTURE \_ \_ \_ 2D, um eindimensionale oder zweidimensionale Textur anzugeben. Der *pname-Parameter* akzeptiert die gleichen Symbole wie [**glTexParameter**](gltexparameter-functions.md)mit den gleichen Interpretationen.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt der *Parameter vorgenommen.*

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





