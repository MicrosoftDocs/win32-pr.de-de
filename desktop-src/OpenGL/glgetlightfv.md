---
title: glGetLightfv-Funktion (Gl.h)
description: Die Funktionen glGetLightfv und glGetLightiv geben Light Source-Parameterwerte zurück. | glGetLightfv-Funktion (Gl.h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- glGetLightfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d642b0d253abca4ea7c5f224353f5544b5307df5237e958c32e37b98ff2e01f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741997"
---
# <a name="glgetlightfv-function"></a>glGetLightfv-Funktion

Die **Funktionen glGetLightfv und** [**glGetLightiv geben**](glgetlightiv.md) Light Source-Parameterwerte zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*light* 
</dt> <dd>

Eine Lichtquelle. Die Anzahl möglicher Beleuchtungen hängt von der Implementierung ab, aber es werden mindestens acht Beleuchtungen unterstützt. Sie werden durch symbolische Namen der Form GL LIGHT i identifiziert, wobei \_ 0 = *i <* GL MAX  \_ \_ LIGHTS.

</dd> <dt>

*pname* 
</dt> <dd>

Ein Light Source-Parameter für *light*. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                            | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Umgebungsstärke der Lichtquelle darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                            | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die diffuse Intensität der Lichtquelle darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                         | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Specular-Intensität der Lichtquelle darstellen. Ganzzahlwerte werden, wenn sie angefordert werden, linear aus der internen Gleitkommadarstellung zugeordnet, damit 1,0 dem positivsten darstellbaren ganzzahligen Wert und -1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet wird. Wenn der interne Wert außerhalb des Bereichs \[ von -1,1 liegt, ist der entsprechende ganzzahlige Rückgabewert \] nicht definiert.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**GL \_ POSITION**</dt> </dl>                                         | Der *Parameter params* gibt vier ganzzahlige Werte oder Gleitkommawerte zurück, die die Position der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem die internen Gleitkommawerte auf den nächsten ganzzahligen Wert gerundet werden. Die zurückgegebenen Werte werden in Augenkoordinaten beibehalten. Sie sind nicht gleich den mit [**glLight**](gllight-functions.md)angegebenen Werten, es sei denn, die Modellansichtsmatrix wurde zum Zeitpunkt des **GlLight-Namens** identifiziert.<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**GL \_ SPOT \_ DIRECTION**</dt> </dl>                      | Der *Parameter params* gibt drei ganzzahlige Werte oder Gleitkommawerte zurück, die die Richtung der Lichtquelle darstellen. Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem die internen Gleitkommawerte auf den nächsten ganzzahligen Wert gerundet werden. Die zurückgegebenen Werte werden in Augenkoordinaten beibehalten. Sie sind nicht gleich den mit **glLight** angegebenen Werten, es sei denn, die Modellansichtsmatrix wurde zum Zeitpunkt des **GlLight-Namens** identifiziert. Obwohl die Spotrichtung normalisiert wird, bevor sie in der Beleuchtungsgleichung verwendet wird, sind die zurückgegebenen Werte die transformierten Versionen der angegebenen Werte vor der Normalisierung.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                         | Der *Parameter params* gibt eine einzelne ganze Zahl oder einen Gleitkommawert zurück, der den Spot-Exponenten des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, wenn er angefordert wird, indem die interne Gleitkommadarstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                               | Der *Parameter params* gibt eine einzelne ganze Zahl oder einen Gleitkommawert zurück, der den Spot-Cutoff-Winkel des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, wenn er angefordert wird, indem die interne Gleitkommadarstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**GL \_ CONSTANT \_ ATTENUATION**</dt> </dl>    | Der *Parameter params* gibt eine einzelne ganze Zahl oder einen Gleitkommawert zurück, der die konstante (nicht entfernungsbezogene) Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, wenn er angefordert wird, indem die interne Gleitkommadarstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**GL \_ \_ LINEARE DÄMPFUNG**</dt> </dl>          | Der *Parameter params* gibt eine einzelne ganze Zahl oder einen Gleitkommawert zurück, der die lineare Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, wenn er angefordert wird, indem die interne Gleitkommadarstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**GL \_ QUADRATISCHE \_ DÄMPFUNG**</dt> </dl> | Der *Parameter params* gibt eine einzelne ganze Zahl oder einen Gleitkommawert zurück, der die quadratische Dämpfung des Lichts darstellt. Ein ganzzahliger Wert wird berechnet, wenn er angefordert wird, indem die interne Gleitkommadarstellung auf die nächste ganze Zahl gerundet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glGetLight-Funktion** gibt in *Parametern* den Wert oder die Werte eines Light Source-Parameters zurück. Der *Lichtparameter* benennt das Licht und ist ein symbolischer Name der Form GL \_ LIGHT *i* für 0 = *i* < GL MAX LIGHTS, wobei GL MAX LIGHTS eine implementierungsabhängige Konstante ist, die größer oder gleich acht \_ \_ \_ \_ ist. Der *pname-Parameter* gibt einen von zehn Light Source-Parametern an, wiederum durch symbolischen Namen.

Es ist immer der Fall, dass GL \_ LIGHT *i* = GL \_ LIGHT0 + *i* ist.

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

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





