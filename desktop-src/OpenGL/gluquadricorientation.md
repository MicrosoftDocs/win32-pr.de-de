---
title: gluQuadricOrientation-Funktion (Glu.h)
description: Die gluQuadricOrientation-Funktion gibt die Innerhalb- oder Außenausrichtung für Quadrrizen an.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937626"
---
# <a name="gluquadricorientation-function"></a>gluQuadricOrientation-Funktion

Die **gluQuadricOrientation-Funktion** gibt die Innerhalb- oder Außenausrichtung für Quadrrizen an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadObject* 
</dt> <dd>

Das Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Ausrichtung* 
</dt> <dd>

Die gewünschte Ausrichtung. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ OUTSIDE**</dt> </dl> | Zeichnen von Quadrieren mit Normals, die nach außen zeigen. Dies ist der Standardwert.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ INSIDE**</dt> </dl>    | Zeichnen von Quadrieren mit Normals, die nach innen zeigen.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluQuadricOrientation-Funktion** gibt an, welche Art von Ausrichtung für quadric-Objekte, die mit **quadObject gerendert** werden, gewünscht wird. Die Interpretation von nach außen und nach innen hängt vom gezeichneten Quadric ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





