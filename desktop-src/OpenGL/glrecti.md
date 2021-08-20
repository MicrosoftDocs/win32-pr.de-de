---
title: glRecti-Funktion (Gl.h)
description: Die glRecti-Funktion zeichnet ein Rechteck.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- glRecti-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRecti
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fa1432cc74dc87165fcddfa5e28542434758e11606d186302fc2cfe3c6453a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491990"
---
# <a name="glrecti-function"></a>glRecti-Funktion

Die **glRecti-Funktion** zeichnet ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRecti(
   GLint x1,
   GLint y1,
   GLint x2,
   GLint y2
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





