---
description: Die AddAfter-Methode fügt ein Element nach der angegebenen Position ein und verwendet die Parameter "p" und "pObj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: CGenericList.AddAfter-Methode (Wxlist.h) – p, pObj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697530"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>CGenericList.AddAfter-Methode (Wxlist.h) – p, pObj-Parameter

Die `AddAfter` -Methode fügt ein Element nach der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*P* 
</dt> <dd>

Position, nach der das Element hinzugefügt werden soll. Wenn *p* **NULL** ist, fügt die -Methode das Element dem Kopf der Liste hinzu.

</dd> <dt>

*pObj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator des eingefügten Elements zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




