---
description: Die AddBefore-Methode fügt ein Element vor der angegebenen Position ein. Diese Methode verwendet die Parameter "p" und "pobj".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Cgenericlist. AddBefore-Methode (wxlist. h)-p, pobj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961786"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Cgenericlist. AddBefore-Methode (wxlist. h)-p, pobj-Parameter

Die- `AddBefore` Methode fügt ein Element vor der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Die Position, an der die Liste eingefügt werden soll. Wenn *p* **null** ist, fügt diese Methode das Element am Ende der Liste hinzu.

</dd> <dt>

*pobj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator für das eingefügte Element zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




