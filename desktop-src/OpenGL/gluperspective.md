---
title: gluPerspective-Funktion (Glu.h)
description: Die gluPerspective-Funktion richtet eine perspektivische Projektionsmatrix ein.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluPerspective-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973040fc9d9f23e6cfba5e30ceea89a1c13cfbaab0071cc7905080cfcdf60f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061588"
---
# <a name="gluperspective-function"></a>gluPerspective-Funktion

Die **gluPerspective-Funktion** richtet eine perspektivische Projektionsmatrix ein.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*folow* 
</dt> <dd>

Das Feld des Ansichtswinkels in Grad in y-Richtung.

</dd> <dt>

*aspect* 
</dt> <dd>

Das Seitenverhältnis, das das Sichtfeld in x-Richtung bestimmt. Das Seitenverhältnis ist das Verhältnis von *x* (Breite) zu *y* (Höhe).

</dd> <dt>

*zNear* 
</dt> <dd>

Der Abstand zwischen dem Viewer und der näheren Clippingebene (immer positiv).

</dd> <dt>

*zFar* 
</dt> <dd>

Der Abstand vom Viewer zur fernen Clippingebene (immer positiv).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluPerspective-Funktion** gibt ein Frustum im Weltkoordinatensystem an. Im Allgemeinen sollte das Seitenverhältnis in **gluPerspective** mit dem Seitenverhältnis des zugeordneten Viewports übereinstimmen. "aspect  = 2.0" bedeutet beispielsweise, dass der Ansichtswinkel des Betrachters in *x* doppelt so breit ist wie in *y.* Wenn der Viewport doppelt so breit wie hoch ist, wird das Bild ohne Verzerrung angezeigt.

Die von **gluPerspective** generierte Matrix wird mit der aktuellen Matrix multipliziert, als ob [**glMultMatrix**](glmultmatrix.md) mit der generierten Matrix aufgerufen würde. Um stattdessen die Perspektivenmatrix in den aktuellen Matrixstapel zu laden, gehen Sie dem Aufruf von **gluPerspective** mit einem Aufruf von [**glLoadIdentity voraus.**](glloadidentity.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





