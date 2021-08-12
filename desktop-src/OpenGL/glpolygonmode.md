---
title: glPolygonMode-Funktion (Gl.h)
description: Die glPolygonMode-Funktion wählt einen Polygonrastermodus aus.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode-Funktion OpenGL
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
ms.openlocfilehash: f040b3e44ee34d819752bae5deffbf1a02f0d38ab1249f2e32de67c262bd5f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615206"
---
# <a name="glpolygonmode-function"></a>glPolygonMode-Funktion

Die **glPolygonMode-Funktion** wählt einen Polygonrastermodus aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Die Polygone, für die *der Modus* gilt. Muss GL \_ FRONT für vordere Polygone, GL \_ BACK für rückwärts gerichtete Polygone oder GL \_ FRONT AND BACK für \_ \_ vordere und hintere Polygone sein.

</dd> <dt>

*mode* 
</dt> <dd>

Die Art und Weise, wie Polygone gerastert werden. Die folgenden Modi sind definiert und können im *Modus* angegeben werden. Der Standardwert ist GL \_ FILL für vordere und hintere Polygone.



| Wert                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**GL \_ POINT**</dt> </dl> | Polygonvertices, die als Anfang eines Begrenzungsrands markiert sind, werden als Punkte gezeichnet. Punktattribute wie GL \_ POINT SIZE und GL POINT SMOOTH steuern die \_ \_ \_ Rasterung der Punkte. Andere Polygonrasterisierungsattribute als GL \_ POLYGON MODE haben keine \_ Auswirkungen.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**GL \_ LINE**</dt> </dl>    | Begrenzungsränder des Polygons werden als Liniensegmente gezeichnet. Sie werden als verbundene Liniensegmente für Zeilenstippling behandelt. der Linienstipplezähler und das Muster werden nicht zwischen Segmenten zurückgesetzt (siehe [**glLineStipple**](gllinestipple.md)). Linienattribute wie GL \_ LINE WIDTH und GL LINE SMOOTH steuern die \_ \_ \_ Rasterung der Linien. Andere Polygonrasterisierungsattribute als GL \_ POLYGON MODE haben keine \_ Auswirkungen.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**GL \_ FILL**</dt> </dl>    | Das Innere des Polygons wird gefüllt. Polygonattribute wie GL \_ POLYGON \_ STIPPLE und GL \_ POLYGON SMOOTH steuern die \_ Rasterung des Polygons.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | Das *Gesicht* oder *der Modus* war kein akzeptierter Wert.<br/>                                                                         |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glPolygonMode-Funktion** steuert die Interpretation von Polygonen für die Rasterung. Der *Gesichtsparameter* beschreibt, für welche *Polygone der Modus* gilt: vordere Polygone (GL \_ FRONT), rückwärts gerichtete Polygone (GL \_ BACK) oder beides (GL \_ FRONT UND \_ \_ BACK). Der Polygonmodus wirkt sich nur auf die endgültige Rasterung von Polygonen aus. Insbesondere werden die Scheitelpunkte eines Polygons angelichtet, und das Polygon wird abgeschnitten und möglicherweise gekäutert, bevor diese Modi angewendet werden.

Rufen Sie auf, um eine Oberfläche mit gefüllten rückwärts gerichteten Polygonen und umrandete Polygone nach oben zu zeichnen.

**glPolygonMode**(GL \_ FRONT, GL \_ LINE);

Scheitelpunkte werden als Begrenzung oder nicht gebunden mit einem Edgeflag markiert. Edgeflags werden intern von OpenGL generiert, wenn Polygone zerlegt werden, und sie können explizit mit [**glEdgeFlag**](gledgeflag-functions.md)festgelegt werden.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glPolygonMode** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ POLYGON \_ MODE

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





