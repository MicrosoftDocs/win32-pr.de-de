---
title: glunewtess-Funktion (glu. h)
description: Die glunewtess-Funktion erstellt ein Mosaik Objekt.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- glunewtess-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338141"
---
# <a name="glunewtess-function"></a>glunewtess-Funktion

Die **glunewtess** -Funktion erstellt ein Mosaik Objekt.

## <a name="syntax"></a>Syntax


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **glunewtess** " erstellt einen Zeiger auf ein neues Mosaik Objekt und gibt diesen zurück. Verweisen Sie auf dieses Objekt, wenn Sie Mosaik Funktionen aufrufen. Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.

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

[**gludeletetess**](gludeletetess.md)
</dt> <dt>

[**glutess beginpolygon**](glubeginpolygon.md)
</dt> <dt>

[*glutesscallback*](glutess.md)
</dt> </dl>

 

 





