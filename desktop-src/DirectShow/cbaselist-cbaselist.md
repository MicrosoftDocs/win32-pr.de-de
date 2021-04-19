---
description: Konstruktormethode.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Cbaselist. cbaselist (TCHAR *, int)-Konstruktor (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355904"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Cbaselist. cbaselist (TCHAR \* , int)-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Aus Effizienzgründen verwaltet die- `CBaseList` Klasse einen Cache von Listen Knoten. Wenn Sie ungefähr wissen, wie viele Elemente in der Liste enthalten sein werden, verwenden Sie diese Version des Konstruktors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




