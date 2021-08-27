---
title: glRectiv-Funktion (Gl.h)
description: Die glRectiv-Funktion zeichnet ein Rechteck.
ms.assetid: 24db6fc0-9b53-4e72-9b12-18ea65409f12
keywords:
- glRectiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRectiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f011748ec66a65511f6cbdcd2342cdf3212d04d3b2ba0507e810eb64293f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036590"
---
# <a name="glrectiv-function"></a>glRectiv-Funktion

Die **glRectiv-Funktion** zeichnet ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRectiv(
   const GLint *v1,
   const GLint *v2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*v1* 
</dt> <dd>

Ein Zeiger auf einen Scheitelpunkt eines Rechtecks.

</dd> <dt>

*v2* 
</dt> <dd>

ein Zeiger auf den gegenüberliegenden Scheitelpunkt des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glRecti-Funktion** unterstützt die effiziente Spezifikation von Rechtecke als zwei Eckpunkte. Jeder Rechteckbefehl nimmt vier Argumente an, die entweder als zwei aufeinander folgende Paare von (*x*, *y*) Koordinaten oder als zwei Zeiger auf Arrays organisiert sind, die jeweils ein Paar *(x*, *y*) enthalten. Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.

Die **glRecti-Funktion**(*x1,* *y1,* *x2,* *y2*) entspricht genau der folgenden Sequenz:

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





