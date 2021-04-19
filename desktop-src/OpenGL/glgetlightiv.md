---
title: glgetlightivfunction (GL. h)
description: Die Funktionen "glgetlightfv" und "glgetlightiv" geben helle Quellparameter Werte zurück. | glgetlightivfunction (GL. h)
ms.assetid: be4316ca-dc49-4bfa-929a-fa25f5057fde
keywords:
- glgetlightivfunction OpenGL
topic_type:
- apiref
api_name:
- glGetLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fdf19bcc27a3ab80e176707ee5b1d481ee6a658
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364326"
---
# <a name="glgetlightiv-function"></a>glgetlightiv-Funktion

Die Funktionen " [**glgetlightfv**](glgetlightfv.md) " und " **glgetlightiv** " geben helle Quellparameter Werte zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetLightiv(
   GLenum light,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*light* 
</dt> <dd>

Eine Lichtquelle. Die Anzahl der möglichen Lichter hängt von der Implementierung ab, aber es werden mindestens acht Leuchten unterstützt. Sie werden durch symbolische Namen der Form GL \_ Light *i* identifiziert, wobei 0 = *i* < GL \_ Max \_ Lights ist.

</dd> <dt>

*pName* 
</dt> <dd>

Ein Light Source-Parameter für *Light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL- \_ AMBIENT**</dt> </dl>                                            | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs Intensität der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL- \_ diffuses**</dt> </dl>                                            | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die diffuse Intensität der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ Glanz**</dt> </dl>                                         | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Glanz Intensität der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist. Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**GL- \_ Position**</dt> </dl>                                         | Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Position der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf den nächstgelegenen ganzzahligen Wert gerundet werden. Die zurückgegebenen Werte werden in den Augen Koordinaten verwaltet. Sie sind nicht gleich den Werten, die mithilfe von [**gllight**](gllight-functions.md)angegeben werden, es sei denn, die Modelview-Matrix wurde zum Zeitpunkt des Aufrufs von **gllight** identifiziert.<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**GL- \_ Spot- \_ Richtung**</dt> </dl>                      | Der Parameter *para* meters gibt drei ganzzahlige Werte oder Gleit Komma Werte zurück, die die Richtung der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf den nächstgelegenen ganzzahligen Wert gerundet werden. Die zurückgegebenen Werte werden in den Augen Koordinaten verwaltet. Sie sind nicht gleich den Werten, die mithilfe von **gllight** angegeben werden, es sei denn, die Modelview-Matrix wurde zum Zeitpunkt des Aufrufs von **gllight** identifiziert. Obwohl die Spot-Richtung normalisiert wird, bevor Sie in der Beleuchtungs Gleichung verwendet wird, sind die zurückgegebenen Werte die transformierten Versionen der angegebenen Werte vor der Normalisierung.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL- \_ Spot- \_ Exponent**</dt> </dl>                         | Der Parameter *para* meters gibt eine einzelne Ganzzahl oder einen Gleit Komma Wert zurück, der den Spot Exponent des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, indem die interne Gleit Komma Darstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL. \_ Spot- \_ cuumff**</dt> </dl>                               | Der Parameter *para* meters gibt eine einzelne Ganzzahl oder einen Gleit Komma Wert zurück, der den Winkel der Licht Spitze des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, indem die interne Gleit Komma Darstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**GL- \_ Konstante \_ Dämpfung**</dt> </dl>    | Der Parameter *para* meters gibt eine einzelne Ganzzahl oder einen Gleit Komma Wert zurück, der die Konstante (nicht Entfernungs bedingte) Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, indem die interne Gleit Komma Darstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**\_lineare \_ Dämpfung von GL**</dt> </dl>          | Der Parameter *para* meters gibt eine einzelne Ganzzahl oder einen Gleit Komma Wert zurück, der die lineare Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, indem die interne Gleit Komma Darstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**GL. \_ quadratische \_ Dämpfung**</dt> </dl> | Der Parameter *para* meters gibt eine einzelne Ganzzahl oder einen Gleit Komma Wert zurück, der die quadratische Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, indem die interne Gleit Komma Darstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glgetlight** " *gibt in Parameter* den Wert oder die Werte eines Light Source-Parameters zurück. Der *Light* -Parameter benennt das Licht und ist ein symbolischer Name der Form GL \_ Light *i* für 0 = *i* < GL \_ Max \_ Lights, wobei GL \_ Max \_ Lights eine Implementierungs abhängige Konstante ist, die größer oder gleich 8 ist. Der *PName* -Parameter gibt einen von zehn Licht Quell Parametern an, wieder nach symbolischen Namen.

Es ist immer der Fall, dass GL \_ Light *i* = GL \_ LIGHT0 + *i*.

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

[**gllight**](gllight-functions.md)
</dt> </dl>

 

 





