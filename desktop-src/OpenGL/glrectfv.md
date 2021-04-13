---
title: glrectfv-Funktion (GL. h)
description: Die Funktion "glrectfv" zeichnet ein Rechteck.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- glrectfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391536"
---
# <a name="glrectfv-function"></a>glrectfv-Funktion

Die Funktion " [**glrectfv**](glrectdv.md) " zeichnet ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
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

Ein Zeiger auf den umgekehrten Scheitelpunkt des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glrectf** -Funktion unterstützt die effiziente Angabe von Rechtecke als zwei Eckpunkte. Jeder Rechteck Befehl benötigt vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*)-Koordinaten oder als zwei Zeiger auf Arrays angeordnet sind, die jeweils ein (*x*, *y*)-Paar enthalten. Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.

Die Funktion " **glrectf**(*x1,* *Y1,* *x2,* *Y2*)" entspricht genau der folgenden Reihenfolge:

**glBegin**(GL- \_ Polygon);

**glVertex2**( *x1,* *Y1* );

**glVertex2**( *x2,* *Y1* );

**glVertex2**( *x2,* *Y2* );

**glVertex2**( *x1,* *Y2* );

**glEnd**();

Beachten Sie Folgendes: Wenn sich der zweite Scheitelpunkt oberhalb und rechts vom ersten Scheitelpunkt befindet, wird das Rechteck mit einem gegen Uhrzeigersinn konstruiert.

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

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





