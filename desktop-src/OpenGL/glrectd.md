---
title: glRectd-Funktion (Gl.h)
description: Die funktion glRectd zeichnet ein Rechteck.
ms.assetid: d5574c22-7ae1-4040-9b95-769693fa41e3
keywords:
- glRectd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRectd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 961b5b9ddf478475806d391d6499eed01fd43e14781f57dcd82e9ff6a1a55a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492170"
---
# <a name="glrectd-function"></a>glRectd-Funktion

Die **funktion glRectd** zeichnet ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRectd(
   GLdouble x1,
   GLdouble y1,
   GLdouble x2,
   GLdouble y2
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

Die  y-Koordinate des Scheitelpunkts eines Rechtecks.

</dd> <dt>

*x2* 
</dt> <dd>

Die  x-Koordinate des gegenüberliegenden Scheitelpunkts des Rechtecks.

</dd> <dt>

*y2* 
</dt> <dd>

Die  y-Koordinate des umgekehrten Scheitelpunkts des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glRectd-Funktion** unterstützt die effiziente Spezifikation von Rechtecke als zwei Eckpunkte. Jeder Rechteckbefehl verwendet vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*) Koordinaten oder als zwei Zeiger auf Arrays organisiert sind, die jeweils ein (*x*, *y*) -Paar enthalten. Das resultierende Rechteck wird in der *Ebene z* = 0 definiert.

Die **Funktion glRectd**(*x1,* *y1,* *x2,* *y2*) entspricht genau der folgenden Sequenz:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Beachten Sie, dass, wenn sich der zweite Scheitelpunkt oberhalb und rechts neben dem ersten Scheitelpunkt befindet, das Rechteck mit einer Windung gegen den Uhrzeigersinn erstellt wird.

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

 

 





