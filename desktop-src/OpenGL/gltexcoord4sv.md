---
title: glTexCoord4sv-Funktion (Gl.h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord4sv-Funktion (Gl.h)
ms.assetid: 8192d896-c099-410b-9df6-21f9b66d910b
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
ms.openlocfilehash: 5ba5d6d4fccb5199c23a745cf29443cd6ef3e92e1a863dc7a247d029bae7fc2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490720"
---
# <a name="gltexcoord4sv-function"></a>glTexCoord4sv-Funktion

Legt die aktuellen Texturkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoord4dv(
   const GLshort *v
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

Die [**funktion glTexCoord**](gltexcoord-functions.md) legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygonvertices zugeordnet sind. Die **glTexCoord-Funktion** gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an. Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. ein Aufruf von glTexCoord2 legt sie auf fest (s, t, 0, 1). Auf ähnliche Weise gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q). Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren. Insbesondere können Sie glTexCoord zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufrufen.**](glend.md) Die folgende Funktion ruft Informationen im Zusammenhang mit **glTexCoord ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ CURRENT TEXTURE \_ \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





