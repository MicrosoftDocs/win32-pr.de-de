---
title: glTexCoord3s-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord3s-Funktion (GL. h)
ms.assetid: 0698c7fe-3a1a-4713-a72b-17d81840251b
keywords:
- glTexCoord3s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057f04fd2a811e7da34c7797dd4ca61ad9b5ff69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870003"
---
# <a name="gltexcoord3s-function"></a>glTexCoord3s-Funktion

Legt die aktuellen Texturkoordinaten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexCoord3s(
   GLshort s,
   GLshort t,
   GLshort r
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* 
</dt> <dd>

Die s-Textur Koordinate.

</dd> <dt>

*t* 
</dt> <dd>

Die t-Textur Koordinate.

</dd> <dt>

*r* 
</dt> <dd>

Die r-Textur Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind. Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an. Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt. Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q). Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren. Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen. Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





