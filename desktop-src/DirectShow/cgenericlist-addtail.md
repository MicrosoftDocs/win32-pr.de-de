---
description: Die AddTail-Methode fügt ein Element am Ende der Liste an.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Cgenericlist. AddTail-Methode (wxlist. h)-pobj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365877"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>Cgenericlist. AddTail-Methode (wxlist. h)-pobj-Parameter

Die- `AddTail` Methode fügt ein Element am Ende der Liste an.

## <a name="syntax"></a>Syntax


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Positionswert für die neue Endposition zurück. Wenn die Methode fehlschlägt, wird **null** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




