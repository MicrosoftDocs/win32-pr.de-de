---
title: glpolygonmode-Funktion (GL. h)
description: Die glpolygonmode-Funktion wählt einen Polygon-rasterisierungsmodus aus.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glpolygonmode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343892"
---
# <a name="glpolygonmode-function"></a>glpolygonmode-Funktion

Die **glpolygonmode** -Funktion wählt einen Polygon-rasterisierungsmodus aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mit* 
</dt> <dd>

Die Polygone, auf die der *Modus* angewendet wird. Muss "GL \_ Front" für Front-on-Polygone, "GL \_ Back" für rückwärts gerichtete Polygone oder "GL \_ Front \_ und \_ Back" für Front-und Back-on-Polygone sein.

</dd> <dt>

*mode* 
</dt> <dd>

Die Art und Weise, wie Polygone rasteriert werden. Die folgenden Modi sind definiert und können im- *Modus* angegeben werden. Der Standardwert ist GL \_ Fill sowohl für Front-als auch für rückwärts gerichtete Polygone.



| Wert                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**GL- \_ Punkt**</dt> </dl> | Polygon Scheitel Punkte, die als Ausgangspunkt eines Begrenzungs Kanten gekennzeichnet sind, werden als Punkte gezeichnet. Die rasterisierung der Punkte wird von Punkt Attributen wie der GL \_ \_ -Punktgröße und dem GL- \_ Punkt \_ glatt gesteuert. Polygon-rasterisierungsattribute außer dem GL- \_ Polygon- \_ Modus haben keine Auswirkung.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**GL- \_ Zeile**</dt> </dl>    | Begrenzungs Kanten des Polygons werden als Liniensegmente gezeichnet. Sie werden als verbundene Liniensegmente für den Zeilen stippling behandelt. der Zeilen stippingcounter und das Muster werden nicht zwischen Segmenten zurückgesetzt (siehe [**glLineStipple**](gllinestipple.md)). Linien Attribute wie GL \_ -Linienstärke \_ und GL- \_ Linien \_ Glättung steuern die rasterisierung der Zeilen. Polygon-rasterisierungsattribute außer dem GL- \_ Polygon- \_ Modus haben keine Auswirkung.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**Ausfüllen von GL \_**</dt> </dl>    | Das Innere des Polygons wird ausgefüllt. Polygon-Attribute, wie z. b. gl \_ \_ -Polygon-Stippel und GL- \_ Polygon, \_ steuern die rasterisierung des Polygons.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Entweder das *Gesicht* oder der *Modus* war kein akzeptierter Wert.<br/>                                                                         |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glpolygonmode** " steuert die Interpretation von Polygonen für die rasterisierung. Der *Face* -Parameter beschreibt, für welchen polygonalmodus gilt: Front-on-Polygone (GL  \_ Front), Back-over-Polygone (GL \_ Back) oder beides (GL \_ Front \_ und \_ Back). Der Polygon Modus wirkt sich nur auf die endgültige rasterisierung von Polygonen aus. Vor allem werden die Scheitel Punkte eines Polygons beleuchtet, und das Polygon wird abgeschnitten, und möglicherweise ist es möglich, bevor diese Modi angewendet werden.

Um eine Oberfläche mit gefüllten, rückwärts gerichteten Polygonen zu zeichnen und Front-End-Polygone zu sehen,

**glpolygonmode**(GL \_ Front, GL \_ Line);

Scheitel Punkte werden mit einem edgeflag als Begrenzung oder nonborder gekennzeichnet. Edge-Flags werden intern von OpenGL generiert, wenn Polygone entfernt werden, und Sie können mithilfe von [**gledgeflag**](gledgeflag-functions.md)explizit festgelegt werden.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glpolygonmode** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Polygon- \_ Modus

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

[**gledgeflag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**gllinestippel**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glpolygonstippel**](glpolygonstipple.md)
</dt> </dl>

 

 





