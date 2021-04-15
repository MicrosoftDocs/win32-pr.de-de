---
title: glrecti-Funktion (GL. h)
description: Die glrecti-Funktion zeichnet ein Rechteck.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- glrecti-Funktion OpenGL
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
ms.openlocfilehash: 9a17512c9720aea1d2b9dcf5c90b0bde4c67b8fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475249"
---
# <a name="glrecti-function"></a>glrecti-Funktion

Die **glrecti** -Funktion zeichnet ein Rechteck.

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

Die *x* -Koordinate des Scheitel Punkts eines Rechtecks.

</dd> <dt>

*y1* 
</dt> <dd>

Die *y* -Koordinate des Scheitel Punkts eines Rechtecks.

</dd> <dt>

*x2* 
</dt> <dd>

Die *x* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.

</dd> <dt>

*Y2* 
</dt> <dd>

Die *y* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glrecti** -Funktion unterstützt die effiziente Angabe von Rechtecke als zwei Eckpunkte. Jeder Rechteck Befehl benötigt vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*)-Koordinaten oder als zwei Zeiger auf Arrays angeordnet sind, die jeweils ein (*x*, *y*)-Paar enthalten. Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.

Die Funktion " **glrecti**(*x1,* *Y1,* *x2,* *Y2*)" entspricht genau der folgenden Reihenfolge:

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

 

 





