---
title: glTexCoord4d-Funktion (Gl.h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord4d-Funktion (Gl.h)
ms.assetid: d9045a2e-81f3-4f63-8eee-e882c586b8fe
keywords:
- glTexCoord4d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fbdd49d6a760e3e1c43fddcd5bcce85418d34ca803569a4c22ab6bea89b266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613749"
---
# <a name="gltexcoord4d-function"></a>glTexCoord4d-Funktion

Legt die aktuellen Texturkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoord4d(
   GLdouble s,
   GLdouble t,
   GLdouble r,
   GLdouble q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* 
</dt> <dd>

Die Texturkoordinate.

</dd> <dt>

*t* 
</dt> <dd>

Die Texturkoordinate t.

</dd> <dt>

*r* 
</dt> <dd>

Die r-Texturkoordinate.

</dd> <dt>

*Q* 
</dt> <dd>

Die q-Texturkoordinate.

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

 

 





