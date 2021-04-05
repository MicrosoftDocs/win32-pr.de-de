---
title: gltexenviv-Funktion (GL. h)
description: Die gltexenviv-Funktion legt einen Texture-Umgebungsparameter fest.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- gltexenviv-Funktion OpenGL
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
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859302"
---
# <a name="gltexenviv-function"></a>gltexenviv-Funktion

Die **gltexenviv** -Funktion legt einen Texture-Umgebungsparameter fest.

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

Eine Textur Umgebung. Muss "GL \_ Texture" sein \_ .

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name eines einwertigen Textur Umgebungs Parameters. Akzeptierte Werte sind der \_ GL \_ -Textur env \_ -Modus und die GL- \_ Textur \_ env- \_ Farbe.

</dd> <dt>

*params* 
</dt> <dd>

Ein Zeiger auf ein Array von Parametern: entweder eine einzelne symbolische Konstante oder eine RGBA-Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *target* oder *PName* war keiner der akzeptierten definierten Werte, oder wenn Parameter einen definierten Konstanten Wert *aufweisen sollten (* basierend auf dem Wert von *PName*), und nicht.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                             |



## <a name="remarks"></a>Bemerkungen

Eine Textur Umgebung gibt an, wie Textur Werte interpretiert werden, wenn ein Fragment strukturiert ist. Der *Ziel* Parameter muss "GL \_ Texture" sein \_ . Der *PName* -Parameter kann entweder der GL- \_ Textur \_ env- \_ Modus oder die GL- \_ Textur \_ env- \_ Farbe sein.

Wenn *PName* den GL- \_ Textur \_ env- \_ Modus  hat, ist der symbolische Name einer Textur Funktion (oder verweist auf diesen). Drei Textur Funktionen sind definiert: GL \_ Modulate, GL \_ Decal und GL \_ Blend.

Eine Textur Funktion wird für das Fragment verwendet, das mit dem Textur bildrwert, der für das Fragment gilt (siehe [**gltexparameter**](gltexparameter-functions.md)), strukturiert werden soll, und erzeugt eine RGBA-Farbe für dieses Fragment. In der folgenden Tabelle wird gezeigt, wie die RGBA-Farbe für jede der drei Textur Funktionen erstellt wird, die ausgewählt werden können. *C* ist ein dreifaches von Farbwerten (RGB), und *ein* ist der zugeordnete Alphawert. Aus einem Textur Bild extrahierte RGBA-Werte liegen im Bereich von \[ 0, 1 \] . Der Index " *f* " bezieht sich auf das eingehende Fragment, *das für das* Textur Bild, den Index " *c* " für die Textur Umgebungs Farbe und "Index *v* " einen Wert, der von der Textur Funktion erzeugt wird.

Ein Textur Bild kann bis zu vier Komponenten pro Textur Element aufweisen (siehe [**glTexImage1D**](glteximage1d.md) und [**glTexImage2D**](glteximage2d.md)). In einem einkomponentenbild gibt lt diese einzelne Komponente an. Ein Image mit zwei Komponenten verwendet *L?*  und *A?* . Ein Image mit drei Komponenten hat nur einen Farbwert, *C?* . Ein Image mit vier Komponenten hat beide den Farbwert *C?*  und ein Alpha Wert *A?* .



<table>
<thead>
<tr class="header">
<th>Anzahl von Komponenten</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1 $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">nicht definiertes $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">nicht definiertes $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em></td>
<td rowspan="2">nicht definiertes $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {Remove} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>A?</em> <em>) C<sub>f</sub> </em> + <em>A?</em> <em>Scher?</em></td>
<td rowspan="2">nicht definiertes $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

Wenn pName eine GL- \_ Textur \_ env-Farbe ist \_ , ist *params* ein Zeiger auf ein Array, das eine aus vier Werten bestehenden RGBA-Farbe enthält. Ganzzahlige Farbkomponenten werden linear interpretiert, sodass die positive ganze Zahl 1,0 und die negativste Ganzzahl "-1,0" zugeordnet wird. Die Werte werden an den Bereich \[ 0, 1 gebunden, \] Wenn Sie angegeben werden. *C <sub>c</sub>* übernimmt diese vier Werte.

Der \_ GL \_ -Textur env \_ -Modus wird standardmäßig auf GL \_ modulate und \_ die Standardfarbe der GL-Textur \_ env \_ auf (0, 0, 0, 0) eingestellt.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexenviv** ab:

[**gltexgetenviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





