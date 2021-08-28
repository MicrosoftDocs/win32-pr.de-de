---
title: glGetMaterialfv-Funktion (Gl.h)
description: Die Funktionen glGetMaterialfv und glGetMaterialiv geben Materialparameter zurück. | glGetMaterialfv-Funktion (Gl.h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- glGetMaterialfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261c8e587b3bc339365d6c1d490bec6b2d9c27c9c4531e08dd1546ee8849baac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741370"
---
# <a name="glgetmaterialfv-function"></a>glGetMaterialfv-Funktion

Die Funktionen **glGetMaterialfv** und [**glGetMaterialiv**](glgetmaterialiv.md) geben Materialparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Gibt an, welches der beiden Materialien abgefragt wird. GL \_ FRONT oder GL BACK werden \_ akzeptiert, die das vordere bzw. das hintere Material darstellen.

</dd> <dt>

*pname* 
</dt> <dd>

Der zurückzugebende Materialparameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                    | Der *parameter-Parameter* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Umgebungsreflektion des Materials darstellen. Ganzzahlige Werte werden bei Anforderung linear aus der internen Gleitkommadarstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ -1,1 \] liegt, ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                    | Der *parameter-Parameter* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die diffuse Reflektion des Materials darstellen. Ganzzahlige Werte werden bei Anforderung linear aus der internen Gleitkommadarstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ -1,1 \] liegt, ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                 | Der *parameter-Parameter* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Glanzreflektion des Materials darstellen. Ganzzahlige Werte werden bei Anforderung linear aus der internen Gleitkommadarstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ -1,1 \] liegt, ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ AUSGABE**</dt> </dl>                 | Der *params-Parameter* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die ausgegebene Lichtstärke des Materials darstellen. Ganzzahlige Werte werden bei Anforderung linear aus der internen Gleitkommadarstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ -1,1 \] liegt, ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-VERTRAUENSWÜRDIGKEIT**</dt> </dl>              | Der *parameter-Parameter* gibt eine ganze Zahl oder einen Gleitkommawert zurück, der den Glanzlichter des Materials darstellt. Ganzzahlige Werte werden bei Anforderung berechnet, indem der interne Gleitkommawert auf den nächsten ganzzahligen Wert gerundet wird.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL \_ COLOR \_ INDEXES**</dt> </dl> | Der *parameter-Parameter* gibt drei ganzzahlige Werte oder Gleitkommawerte zurück, die die Umgebungs-, Diffuse- und Glanzindizes des Materials darstellen. Verwenden Sie diese Indizes nur für die Farbindexbeleuchtung. (Die anderen Parameter werden alle nur für RGBA-Beleuchtung verwendet.) Ganzzahlige Werte werden bei Anforderung berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/>                                                                                            |



 

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
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *query* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetMaterial-Funktion** gibt in *den* Wert oder die Werte des Parameters *pname* des *Materialgesichts* zurück.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Parameter* vorgenommen.

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

 

 





