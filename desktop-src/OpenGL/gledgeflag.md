---
title: gledgeflag-Funktion (GL. h)
description: Markiert Kanten entweder als Begrenzung oder als nicht Grenze. | gledgeflag-Funktion (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- gledgeflag-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364318"
---
# <a name="gledgeflag-function"></a>gledgeflag-Funktion

Markiert Kanten entweder als Begrenzung oder als nicht Grenze.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flag* 
</dt> <dd>

Gibt den aktuellen Edge-Flag-Wert an, entweder **true** oder **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jeder Scheitelpunkt eines Polygon, eines separaten Dreiecks oder eines separaten vierends, das zwischen einem [**glBegin**](/windows/desktop/OpenGL/glbegin)- / [**glEnd**](/windows/desktop/OpenGL/glend) -Paar angegeben ist, wird als Start einer Grenze oder einer nicht-Begrenzungs Kante gekennzeichnet. Wenn das aktuelle Edge-Flag **true** ist, wenn der Scheitelpunkt angegeben ist, wird der Scheitelpunkt als Anfang eines Begrenzungs Rands markiert. Wenn das aktuelle Edge-Flag den Wert **false** hat, wird der Scheitelpunkt als Anfang eines nicht Begrenzungs Randes markiert. Die Funktion **gledgeflag** legt das edgeflag auf **true** fest, wenn Flag ungleich 0 (null) ist, andernfalls **false** .

Die Scheitel Punkte verbundener Dreiecke und verbundener Vierecke werden immer als Grenze gekennzeichnet, unabhängig vom Wert des Edge-Flags.

Border-und nonborder-edgeflags für Scheitel Punkte sind nur dann von Bedeutung, wenn der GL- \_ Polygon \_ Modus auf GL \_ Point oder GL Line festgelegt ist \_ Siehe [**glpolygonmode**](/windows/desktop/OpenGL/glpolygonmode).

Anfänglich ist das Edge-Flag " **true**".

Das aktuelle Edge-Flag kann jederzeit aktualisiert werden. Insbesondere kann **gledgeflag** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](/windows/desktop/OpenGL/glend)aufgerufen werden.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **gledgeflag** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Edge- \_ Flag

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

