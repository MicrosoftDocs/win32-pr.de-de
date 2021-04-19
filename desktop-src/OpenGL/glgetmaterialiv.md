---
title: glgetmaterialiv-Funktion (GL. h)
description: Die Funktionen "glgetmaterialfv" und "glgetmaterialiv" geben Materialparameter zurück. | glgetmaterialiv-Funktion (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glgetmaterialiv-Funktion OpenGL
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
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370375"
---
# <a name="glgetmaterialiv-function"></a>glgetmaterialiv-Funktion

Die Funktionen " [**glgetmaterialfv**](glgetmaterialfv.md) " und " **glgetmaterialiv** " geben Materialparameter zurück.

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

*mit* 
</dt> <dd>

Gibt an, welches der beiden Materialien abgefragt wird. GL \_ -Front-oder-GL \_ -Back wird akzeptiert und repräsentiert jeweils die Vorder-bzw. Back Materialien.

</dd> <dt>

*pName* 
</dt> <dd>

Der zurück zugebende Materialparameter. Die folgenden Werte werden akzeptiert.



| Wert                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL- \_ AMBIENT**</dt> </dl>                    | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs Reflektion des Materials darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL- \_ diffuses**</dt> </dl>                    | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die diffuse Reflektion des Materials darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ Glanz**</dt> </dl>                 | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Glanz Reflektion des Materials darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ -Ausgabe**</dt> </dl>                 | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die ausgegebene helle Intensität des Materials darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ .**</dt> </dl>              | Der Parameter *para* meters gibt eine ganze Zahl oder einen Gleit Komma Wert zurück, der den Glanz Exponenten des Materials darstellt. Ganzzahlige Werte werden, wenn angefordert, berechnet, indem der interne Gleit Komma Wert auf den nächsten ganzzahligen Wert gerundet wird.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL- \_ Farb \_ Indizes**</dt> </dl> | Der Parameter *para* meters gibt drei ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs-, diffusen und Glanz Indizes des Materials darstellen. Verwenden Sie diese Indizes nur für die Farb Index Beleuchtung. (Die anderen Parameter werden nur für die RGBA-Beleuchtung verwendet.) Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.<br/>                                                                                            |



 

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
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* oder die *Abfrage* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetmaterial** " gibt in den *para* Metern den Wert oder die Werte des Parameters " *PName* " der materiellen *Fläche* zurück.

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

[**glmaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





