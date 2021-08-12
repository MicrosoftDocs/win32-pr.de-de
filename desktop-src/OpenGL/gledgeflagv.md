---
title: glEdgeFlagv-Funktion (Gl.h)
description: Kennzeichnet Kanten entweder als Begrenzung oder als nicht gebunden. | glEdgeFlagv-Funktion (Gl.h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9622cb3c7d80d241d0f12957094a06980f5fcf7f28b4f95eaa0de1595b34d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616532"
---
# <a name="gledgeflagv-function"></a>glEdgeFlagv-Funktion

Kennzeichnet Kanten entweder als Begrenzung oder als nicht gebunden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flag* 
</dt> <dd>

Gibt einen Zeiger auf ein Array an, das ein einzelnes boolesches Element enthält, das den aktuellen Edgeflagwert ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Scheitelpunkt eines Polygons, eines separaten Dreiecks oder eines separaten Quadernatrals, der zwischen einem [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd-Paar**](/windows/desktop/OpenGL/glend) angegeben ist, wird als Anfang einer Begrenzung oder eines nicht gebundenen Rands markiert. Wenn das aktuelle Edgeflag **TRUE** ist, wenn der Scheitelpunkt angegeben wird, wird der Scheitelpunkt als Anfang eines Begrenzungsrands markiert. Wenn das aktuelle Edgeflag **FALSE** ist, wird der Scheitelpunkt als Anfang eines nicht gebundenen Edge markiert. Die **glEdgeFlagv-Funktion** legt das Edgeflag auf **TRUE** fest, wenn das Flag ungleich null ist, andernfalls **FALSE.**

Die Scheitelpunkte von verbundenen Dreiecken und verbundenen Quadernatralen werden immer als Begrenzung markiert, unabhängig vom Wert des Edgeflags.

Begrenzungsflags und nicht gebundene Randflags auf Scheitelpunkten sind nur dann von Bedeutung, wenn GL \_ POLYGON MODE auf GL POINT oder GL LINE festgelegt \_ \_ \_ ist. Siehe [**glPolygonMode.**](/windows/desktop/OpenGL/glpolygonmode)

Anfänglich ist das Edgeflagbit **TRUE.**

Das aktuelle Edgeflag kann jederzeit aktualisiert werden. Insbesondere kann **glEdgeFlagv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](/windows/desktop/OpenGL/glend)aufgerufen werden.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glEdgeFlagv ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

