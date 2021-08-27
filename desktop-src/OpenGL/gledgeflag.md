---
title: glEdgeFlag-Funktion (Gl.h)
description: Kennzeichnet Ränder entweder als Grenze oder als nicht eingehend. | glEdgeFlag-Funktion (Gl.h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- glEdgeFlag-Funktion OpenGL
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
ms.openlocfilehash: 9c7f78575c79b3da5b48125203d88c9b20e7eb1dc11ee860deea01dfa7dcea28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081590"
---
# <a name="gledgeflag-function"></a>glEdgeFlag-Funktion

Kennzeichnet Ränder entweder als Grenze oder als nicht eingehend.

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

Gibt den aktuellen Edgeflagwert an, entweder **TRUE** oder **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Scheitelpunkt eines Polygons, eines separaten Dreiecks oder eines separaten quadrierten Dreiecks, der zwischen einem [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd-Paar**](/windows/desktop/OpenGL/glend) angegeben ist, wird entweder als Anfang einer Begrenzung oder eines nicht gebundenen Edge markiert. Wenn das aktuelle Edgeflag **true ist,** wenn der Scheitelpunkt angegeben wird, wird der Scheitelpunkt als Anfang eines Begrenzungsrands markiert. Wenn das aktuelle Edgeflag **FALSE ist,** wird der Scheitelpunkt als Anfang eines nicht ausgehenden Edges markiert. Die **glEdgeFlag-Funktion** legt das Edgeflag auf **TRUE fest,** wenn das Flag ungleich 0 (null) ist, andernfalls **FALSE.**

Die Scheitelzeichen von verbundenen Dreiecken und verbundenen Quadrierten sind immer als Begrenzung gekennzeichnet, unabhängig vom Wert des Edgeflags.

Begrenzungsflags und nichtboundäre Edgeflags für Scheitelpunkt sind nur dann von Bedeutung, wenn GL POLYGON MODE auf \_ GL POINT oder GL LINE festgelegt \_ \_ \_ ist. Siehe [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Anfangs ist das Edgeflagbit **TRUE.**

Das aktuelle Edgeflag kann jederzeit aktualisiert werden. Insbesondere kann **glEdgeFlag zwischen** einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd aufgerufen werden.**](/windows/desktop/OpenGL/glend)

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glEdgeFlag ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

