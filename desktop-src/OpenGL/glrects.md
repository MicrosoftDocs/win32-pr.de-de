---
title: glRects-Funktion (Gl.h)
description: Die glRects-Funktion zeichnet ein Rechteck.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- glRects-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e7207f46ec8bb25f22b3b620f00994bf88e929dac318abf14bd09af78cd3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937920"
---
# <a name="glrects-function"></a>glRects-Funktion

Die **glRects-Funktion** zeichnet ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x1* 
</dt> <dd>

Die  x-Koordinate des Scheitelpunkts eines Rechtecks.

</dd> <dt>

*y1* 
</dt> <dd>

Die *y-Koordinate* des Scheitelpunkts eines Rechtecks.

</dd> <dt>

*x2* 
</dt> <dd>

Die  x-Koordinate des gegenüberliegenden Scheitelpunkts des Rechtecks.

</dd> <dt>

*y2* 
</dt> <dd>

Die *y-Koordinate* des gegenüberliegenden Scheitelpunkts des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glRects-Funktion** unterstützt die effiziente Spezifikation von Rechtecke als zwei Eckpunkte. Jeder Rechteckbefehl nimmt vier Argumente an, die entweder als zwei aufeinander folgende Paare von (x, *y*) Koordinaten oder als zwei Zeiger auf Arrays organisiert sind, die jeweils ein Paar *(x*, *y)* enthalten. Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.

Die **glRects-Funktion**(*x1,* *y1,* *x2,* *y2*) entspricht genau der folgenden Sequenz:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Beachten Sie, dass, wenn sich der zweite Scheitelpunkt über und rechts vom ersten Scheitelpunkt befindet, das Rechteck mit einem gegen den Uhrzeigersinn gewindet wird.

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

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





