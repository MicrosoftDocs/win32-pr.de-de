---
title: gludeletequadric-Funktion (glu. h)
description: Die Funktion "gludeletequadric" zerstört ein Quadric-Objekt.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gludeletequadric-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742232"
---
# <a name="gludeletequadric-function"></a>gludeletequadric-Funktion

Die Funktion " **gludeletequadric** " zerstört ein Quadric-Objekt.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*state* 
</dt> <dd>

Das zu zerstörende quadrische Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gludeletequadric** " zerstört das Quadric-Objekt und gibt den verwendeten Arbeitsspeicher frei. Nachdem Sie " **gludeletequadric**" aufgerufen haben, können Sie den *Zustand* nicht mehr verwenden.

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
</dt> </dl>

 

 





