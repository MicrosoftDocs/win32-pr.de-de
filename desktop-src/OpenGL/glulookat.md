---
title: glulookat-Funktion (glu. h)
description: Die Funktion "glulookat" definiert eine Anzeige Transformation.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- glulookat-Funktion OpenGL
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
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859301"
---
# <a name="glulookat-function"></a>glulookat-Funktion

Die Funktion " **glulookat** " definiert eine Anzeige Transformation.

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

Die Position des Augen Punkts.

</dd> <dt>

*pipey* 
</dt> <dd>

Die Position des Augen Punkts.

</dd> <dt>

*pipez* 
</dt> <dd>

Die Position des Augen Punkts.

</dd> <dt>

*CenterX* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*CenterY* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*CenterZ* 
</dt> <dd>

Die Position des Bezugspunkts.

</dd> <dt>

*UPX* 
</dt> <dd>

Die Richtung des aufwärts Vektors.

</dd> <dt>

*UPY* 
</dt> <dd>

Die Richtung des aufwärts Vektors.

</dd> <dt>

*UPZ* 
</dt> <dd>

Die Richtung des aufwärts Vektors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glulookat** " erstellt eine von einem Augen Punkt abgeleitete Anzeige Matrix, einen Bezugspunkt, der den Mittelpunkt der Szene angibt, und einen aufwärts Vektor. Die Matrix ordnet den Verweis Punkt der negativen z-Achse und dem Augenblick auf den Ursprung zu. Wenn Sie also eine typische Projektions Matrix verwenden, wird der Mittelpunkt der Szene der Mitte des Viewports zugeordnet. Entsprechend wird die Richtung, die durch den auf die Anzeige Ebene projizierten aufwärts Vektor beschrieben wird, der positiven y-Achse zugeordnet, sodass Sie im Viewport nach oben zeigt. Der Up-Vektor darf nicht parallel zum Bezugspunkt für die Sichtlinie gleich sein.

Die von " **glulookat** " generierte Matrix stellt die aktuelle Matrix dar.

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

[**gluperspective**](gluperspective.md)
</dt> </dl>

 

 





