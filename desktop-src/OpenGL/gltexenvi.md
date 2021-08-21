---
title: glTexEnvi-Funktion (Gl.h)
description: Die glTexEnvi-Funktion legt einen Texturumgebungsparameter fest.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- glTexEnvi-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c976eec51bed7087b1202ae4e4fd9a07435bfa4d6fd0d1fe2b964426bdf0ba5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490600"
---
# <a name="gltexenvi-function"></a>glTexEnvi-Funktion

Die **glTexEnvi-Funktion** legt einen Texturumgebungsparameter fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
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

Der symbolische Name eines Umgebungsparameters für eine einwertige Textur. Muss GL \_ TEXTURE \_ ENV \_ MODE sein.

</dd> <dt>

*param* 
</dt> <dd>

Eine einzelne symbolische Konstante, eine von GL \_ MODULATE, GL \_ DECAL, GL \_ BLEND oder GL \_ REPLACE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *pname* war keiner der akzeptierten definierten Werte, oder wenn *params* einen definierten konstanten Wert aufweisen sollten (basierend auf dem Wert von *pname*) und nicht.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                             |



## <a name="remarks"></a>Hinweise

Eine Texturumgebung gibt an, wie Texturwerte interpretiert werden, wenn ein Fragment texturiert wird. Der *Zielparameter* muss GL \_ TEXTURE \_ ENV sein. Der *pname-Parameter* ist GL \_ TEXTURE \_ ENV \_ MODE. Es werden drei Texturfunktionen definiert: GL \_ MODULATE, GL \_ DECAL und GL \_ BLEND.

Eine Texturfunktion wirkt auf das Fragment, das mithilfe des Texturbildwerts texturiert werden soll, der für das Fragment gilt (siehe [**glTexParameter)**](gltexparameter-functions.md)und erzeugt eine RGBA-Farbe für dieses Fragment. Die folgende Tabelle zeigt, wie die RGBA-Farbe für jede der drei Texturfunktionen erzeugt wird, die ausgewählt werden können. *C* ist ein Triple aus Farbwerten (RGB), und *A* ist der zugeordnete Alphawert. RGBA-Werte, die aus einem Texturbild extrahiert werden, liegen im Bereich \[ von 0, \] 1. Der *Tiefgestellte f* bezieht sich auf das eingehende Fragment, den Index *t* für das Texturbild, das Tiefskript *c* auf die Texturumgebungsfarbe und subscript *v* gibt einen von der Texturfunktion erzeugten Wert an.

Ein Texturbild kann bis zu vier Komponenten pro Texturelement enthalten (siehe [**glTexImage1D**](glteximage1d.md) und [**glTexImage2D**](glteximage2d.md)). In einem Einkomponentenimage gibt Lt diese einzelne Komponente an. Ein Bild mit zwei Komponenten verwendet *L?*  und *A?* . Ein Bild mit drei Komponenten hat nur einen Farbwert, *C?* . Ein Bild mit vier Komponenten verfügt über einen Farbwert *C?*  und einen Alphawert *A?* .



<table>
<thead>
<tr class="header">
<th>Anzahl der Komponenten</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 - <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

\_Der \_ GL TEXTURE-ENV-MODUS \_ ist standardmäßig auf GL \_ MODULATE eingestellt.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glTexEnvi** ab:

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





