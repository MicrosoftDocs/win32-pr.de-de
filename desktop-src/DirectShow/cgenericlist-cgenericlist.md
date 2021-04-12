---
description: Erfahren Sie mehr über die Konstruktormethode für cgenericlist. cgenericlist (wxlist. h). Diese Methode verwendet die Parameter "pname" und "IItems".
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Cgenericlist. cgenericlist-Konstruktor (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356197"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName, IItems-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen der Liste.

</dd> <dt>

*IItems* 
</dt> <dd>

Größe des Knoten Caches.

</dd> <dt>

*Baustein* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*balert* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Aus Effizienzgründen verwaltet die- `CGenericList` Klasse einen Cache von Listen Knoten. Wenn Sie ungefähr wissen, wie viele Elemente in der Liste enthalten sein werden, verwenden Sie diese Version des Konstruktors.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




