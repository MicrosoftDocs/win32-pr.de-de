---
title: glTexEnviv-Funktion (Gl.h)
description: Die glTexEnviv-Funktion legt einen Texturumgebungsparameter fest.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- glTexEnviv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d77cee8aeec55aa09ead5df227fd018d14d6682e08a047d40a1121a11839083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519760"
---
# <a name="gltexenviv-function"></a>glTexEnviv-Funktion

Die **glTexEnviv-Funktion** legt einen Texturumgebungsparameter fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
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

Der symbolische Name eines Umgebungsparameters für eine einwertige Textur. Akzeptierte Werte sind GL \_ TEXTURE \_ ENV \_ MODE und GL TEXTURE \_ \_ ENV \_ COLOR.

</dd> <dt>

*params* 
</dt> <dd>

Ein Zeiger auf ein Array von Parametern: entweder eine einzelne symbolische Konstante oder eine RGBA-Farbe.

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

Eine Texturumgebung gibt an, wie Texturwerte interpretiert werden, wenn ein Fragment texturiert wird. Der *Zielparameter* muss GL \_ TEXTURE \_ ENV sein. Der *Parameter pname* kann entweder GL \_ TEXTURE \_ ENV \_ MODE oder GL TEXTURE \_ \_ ENV \_ COLOR sein.

Wenn *pname* gl \_ TEXTURE \_ ENV MODE ist, ist \_ *params* (oder zeigt auf) den symbolischen Namen einer Texturfunktion. Es werden drei Texturfunktionen definiert: GL \_ MODULATE, GL \_ DECAL und GL \_ BLEND.

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
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 - <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

Wenn pname GL \_ TEXTURE \_ ENV \_ COLOR ist, ist *params* ein Zeiger auf ein Array, das eine RGBA-Farbe enthält, die aus vier Werten besteht. Ganzzahlige Farbkomponenten werden linear interpretiert, sodass die positivste ganze Zahl 1,0 und die negativste ganze Zahl -1,0 zugeordnet wird. Die Werte werden an den Bereich \[ 0 und 1 klammern, \] wenn sie angegeben werden. *C <sub>c</sub>* nimmt diese vier Werte an.

\_Der \_ GL TEXTURE-ENV-MODUS \_ ist standardmäßig auf GL \_ MODULATE und GL TEXTURE \_ \_ ENV \_ COLOR standardmäßig auf (0, 0, 0, 0) eingestellt.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glTexEnviv** ab:

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

 

 





