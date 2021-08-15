---
title: glGetMaterialiv-Funktion (Gl.h)
description: Die Funktionen glGetMaterialfv und glGetMaterialiv geben Materialparameter zurück. | glGetMaterialiv-Funktion (Gl.h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glGetMaterialiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df6babcac908d59c5a5a51b0a23736b760ed25ec542f58339182d3a7536050be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360074"
---
# <a name="glgetmaterialiv-function"></a>glGetMaterialiv-Funktion

Die [**Funktionen glGetMaterialfv**](glgetmaterialfv.md) und **glGetMaterialiv geben** Materialparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Gibt an, welches der beiden Materialien abgefragt wird. GL \_ FRONT bzw. GL \_ BACK werden akzeptiert, die die Vorder- bzw. Hintergrundmaterialien darstellen.

</dd> <dt>

*pname* 
</dt> <dd>

Der zurückzukehrende material-Parameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                    | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Umgebungsreflektoranz des Materials darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                    | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die diffuse Reflektoranz des Materials darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                 | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Glanzreflektor des Materials darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_GL-FEHLER**</dt> </dl>                 | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die ausgegebene Lichtstärke des Materials darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-GL-SCHLÄFRIGKEIT**</dt> </dl>              | Der *Parameter params* gibt eine ganze Zahl oder einen Gleitkommawert zurück, der den Specular Exponent des Materials darstellt. Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem der interne Gleitkommawert auf den nächsten ganzzahligen Wert gerundet wird.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_ \_ GL-FARBINDIZES**</dt> </dl> | Der *Parameter params* gibt drei ganzzahlige Werte oder Gleitkommawerte zurück, die die Umgebungs-, Diffusen- und Specular-Indizes des Materials darstellen. Verwenden Sie diese Indizes nur für die Farbindexbeleuchtung. (Die anderen Parameter werden alle nur für RGBA-Beleuchtung verwendet.) Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *query* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetMaterial-Funktion** gibt in *Parametern* den Wert oder die Werte des Parameters *pname des* materialen Gesichts *zurück.*

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





