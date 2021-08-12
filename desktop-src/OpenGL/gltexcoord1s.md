---
title: glTexCoord1s-Funktion (Gl.h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord1s-Funktion (Gl.h)
ms.assetid: bf84c800-4082-466b-9999-777f0772cd7c
keywords:
- glTexCoord1s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43de74d0aedb40175a49dac79b9ac85b0d08a623eae2c5aaf593f4560083821c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613903"
---
# <a name="gltexcoord1s-function"></a>glTexCoord1s-Funktion

Legt die aktuellen Texturkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoord1s(
   GLshort s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* 
</dt> <dd>

Die Texturkoordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**funktion glTexCoord**](gltexcoord-functions.md) legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygonvertices zugeordnet sind. Die **glTexCoord-Funktion** gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an. Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. Ein Aufruf von glTexCoord2 legt sie auf fest (s, t, 0, 1). Auf ähnliche Weise gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q). Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren. Insbesondere können Sie glTexCoord zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufrufen.**](glend.md) Die folgende Funktion ruft Informationen im Zusammenhang mit **glTexCoord ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ CURRENT TEXTURE \_ \_ COORDS

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

 

 





