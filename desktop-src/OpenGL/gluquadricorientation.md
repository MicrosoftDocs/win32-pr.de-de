---
title: gluquadricorientation-Funktion (glu. h)
description: Die Funktion "gluquadricorientation" gibt die Ausrichtung innerhalb oder außerhalb von viercs an.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluquadricorientation-Funktion OpenGL
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
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739792"
---
# <a name="gluquadricorientation-function"></a>gluquadricorientation-Funktion

Die Funktion " **gluquadricorientation** " gibt die Ausrichtung innerhalb oder außerhalb von viercs an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadobject* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*orientation* 
</dt> <dd>

Die gewünschte Ausrichtung. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**Glu \_ außerhalb**</dt> </dl> | Zeichnen von viercs mit normalen, die nach außen zeigen. Dies ist der Standardwert.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**Glu \_ in**</dt> </dl>    | Zeichnen von viercs mit normalen, die nach innen zeigen.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluquadricorientation** " gibt an, welche Art von Ausrichtung für mit **quadobject** gerenderten viercs gewünscht ist. Die Interpretation von außen und innen hängt von der Quadric ab, die gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**gluquadricdrawstyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluquadricnormals**](gluquadricnormals.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> </dl>

 

 





