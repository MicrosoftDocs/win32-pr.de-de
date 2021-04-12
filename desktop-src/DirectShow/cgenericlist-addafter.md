---
description: Die AddAfter-Methode fügt ein Element nach der angegebenen Position ein und verwendet die Parameter "p" und "pobj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Cgenericlist. AddAfter-Methode (wxlist. h)-p, pobj-Parameter
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356156"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Cgenericlist. AddAfter-Methode (wxlist. h)-p, pobj-Parameter

Die- `AddAfter` Methode fügt ein Element nach der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Die Position, an der das Element hinzugefügt werden soll. Wenn *p* **null** ist, fügt die Methode das Element am Anfang der Liste hinzu.

</dd> <dt>

*pobj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator des eingefügten Elements zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




