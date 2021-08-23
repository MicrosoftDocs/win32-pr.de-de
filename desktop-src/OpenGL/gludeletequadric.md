---
title: gluDeleteQuadric-Funktion (Glu.h)
description: Die gluDeleteQuadric-Funktion zerstört ein quadriertes Objekt.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric-Funktion OpenGL
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
ms.openlocfilehash: ad0c12bd77d3d8b7f7de641671916bb8a901d29d812dfa4e9af6ef116984a128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519620"
---
# <a name="gludeletequadric-function"></a>gluDeleteQuadric-Funktion

Die **gluDeleteQuadric-Funktion** zerstört ein quadriertes Objekt.

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

Das quadrierte Objekt, das zerstört werden soll (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluDeleteQuadric-Funktion** zerstört das quadrierte Objekt und gibt den verwendeten Arbeitsspeicher frei. Nachdem Sie **gluDeleteQuadric** aufgerufen haben, können Sie *den Zustand* nicht mehr verwenden.

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
</dt> </dl>

 

 





