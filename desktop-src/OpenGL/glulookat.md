---
title: gluLookAt-Funktion (Glu.h)
description: Die gluLookAt-Funktion definiert eine Ansichtstransformation.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b21d0cb2fac6573ab2999eb96b2af8b1ecb670f4e51d1ffd2ad91ba001c9ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675300"
---
# <a name="glulookat-function"></a>gluLookAt-Funktion

Die **gluLookAt-Funktion** definiert eine Ansichtstransformation.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*eyex* 
</dt> <dd>

Die Position des Augenpunkts.

</dd> <dt>

*eyey* 
</dt> <dd>

Die Position des Augenpunkts.

</dd> <dt>

*eyez* 
</dt> <dd>

Die Position des Augenpunkts.

</dd> <dt>

*Centerx* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*Centery* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*centerz* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*Upx* 
</dt> <dd>

Die Richtung des Auf-Oben-Vektors.

</dd> <dt>

*upy* 
</dt> <dd>

Die Richtung des Auf-Oben-Vektors.

</dd> <dt>

*Upz* 
</dt> <dd>

Die Richtung des Auf-Oben-Vektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluLookAt-Funktion** erstellt eine von einem Augenpunkt abgeleitete Anzeigematrix, einen Bezugspunkt, der den Mittelpunkt der Szene angibt, und einen Auf-Oben-Vektor. Die Matrix ordnet den Bezugspunkt der negativen Z-Achse und den Augenpunkt dem Ursprung zu. Wenn Sie also eine typische Projektionsmatrix verwenden, wird der Mittelpunkt der Szene der Mitte des Viewports angezeigt. Auf ähnliche Weise wird die von dem auf die Anzeigeebene projizierte Aufwärtsvektor beschriebene Richtung der positiven y-Achse zugeordnet, sodass sie im Viewport nach oben zeigt. Der Auf-Oben-Vektor darf nicht parallel zur Sichtlinie vom Auge zum Bezugspunkt sein.

Die von **gluLookAt** generierte Matrix postmultipliert die aktuelle Matrix.

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





