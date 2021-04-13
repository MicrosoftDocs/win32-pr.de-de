---
title: gluperspective-Funktion (glu. h)
description: Die Funktion "gluperspective" richtet eine perspektivische Projektions Matrix ein.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluperspective-Funktion OpenGL
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
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392109"
---
# <a name="gluperspective-function"></a>gluperspective-Funktion

Die Funktion " **gluperspective** " richtet eine perspektivische Projektions Matrix ein.

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

*fovy* 
</dt> <dd>

Das Feld des Ansichts Winkels in Grad in y-Richtung.

</dd> <dt>

*aspect* 
</dt> <dd>

Das Seitenverhältnis, das das Feld der Sicht in der x-Richtung bestimmt. Das Seitenverhältnis ist das Verhältnis von *x* (Width) zu *y* (Height).

</dd> <dt>

*znear* 
</dt> <dd>

Der Abstand zwischen dem Viewer und der Near Clipping-Ebene (immer positiv).

</dd> <dt>

*zfar* 
</dt> <dd>

Der Abstand zwischen dem Viewer und der weit entfernten Clippingebene (immer positiv).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluperspective** " gibt eine Anzeige von "Frustum" im Weltkoordinaten System an. Im Allgemeinen sollte das Seitenverhältnis in " **gluperspective** " dem Seitenverhältnis des zugeordneten Viewports entsprechen. *Aspekt* = 2,0 bedeutet beispielsweise, dass der Anzeige Winkel des Viewers *doppelt so breit wie in* *y* ist. Wenn der Viewport doppelt so breit ist, wie er hoch ist, wird das Bild ohne Verzerrung angezeigt.

Die von " **gluperspective** " generierte Matrix wird mit der aktuellen Matrix multipliziert, so als ob " [**glmultmatrix**](glmultmatrix.md) " mit der generierten Matrix aufgerufen wurde. Wenn Sie stattdessen die Perspektiven Matrix auf den aktuellen Matrix Stapel laden möchten, stellen Sie dem aufzurufenden **gluperspective** -Befehl den Befehl " [**glLoadIdentity**](glloadidentity.md)" voran.

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

[**glfrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glmultmatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





