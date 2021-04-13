---
title: gluOrtho2D-Funktion (glu. h)
description: Die gluOrtho2D-Funktion definiert eine 2D-Projektions Matrix (orthografische).
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391500"
---
# <a name="gluortho2d-function"></a>gluOrtho2D-Funktion

Die **gluOrtho2D** -Funktion definiert eine 2D-Projektions Matrix (orthografische).

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*linken* 
</dt> <dd>

Die Koordinate für die linke vertikale Clippingebene.

</dd> <dt>

*Richting* 
</dt> <dd>

Die Koordinate für die Rechte vertikale Clippingebene.

</dd> <dt>

*top* 
</dt> <dd>

Die Koordinate für die obere horizontale Clippingebene.

</dd> <dt>

*unten* 
</dt> <dd>

Die Koordinate für die untere horizontale Clippingebene.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **gluOrtho2D** -Funktion richtet einen zweidimensionalen orthografischen Anzeigebereich ein. Dies entspricht dem Aufrufen von [**glortho**](glortho.md) mit Near = 1 und far = 1.

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

[**glortho**](glortho.md)
</dt> <dt>

[**gluperspective**](gluperspective.md)
</dt> </dl>

 

 





