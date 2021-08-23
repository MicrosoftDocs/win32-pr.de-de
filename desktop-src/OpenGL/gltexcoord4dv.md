---
title: glTexCoord4dv-Funktion (Gl.h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord4dv-Funktion (Gl.h)
ms.assetid: 43d3fb1c-c1cf-4f81-aac2-24a5b4c5b29d
keywords:
- glTexCoord4dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d5e2fdfb25d11c2834de3b4cbe164baf3b830e4557ebbdcb0e7792f0ef4252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777840"
---
# <a name="gltexcoord4dv-function"></a>glTexCoord4dv-Funktion

Legt die aktuellen Texturkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoord4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*V* 
</dt> <dd>

Ein Zeiger auf ein Array von vier Elementen, das wiederum die Texturkoordinaten s, t, r und q angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**glTexCoord-Funktion**](gltexcoord-functions.md) legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygonvertices zugeordnet sind. Die **glTexCoord-Funktion** gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an. Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. ein Aufruf von glTexCoord2 legt diese auf (s, t, 0, 1) fest. Ebenso gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q). Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren. Insbesondere können Sie glTexCoord zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufrufen. Die folgende Funktion ruft Informationen im Zusammenhang mit **glTexCoord** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ TEXTURE \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





