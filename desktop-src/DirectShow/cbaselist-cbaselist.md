---
description: 'CBaseList.CBaseList(TCHAR, \* INT)-Konstruktor : Konstruktormethode.'
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: CBaseList.CBaseList(TCHAR*, INT)-Konstruktor (Wxlist.h)
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
ms.openlocfilehash: 5bd3462da5b8403f4db8f4727c0baa0a825e0db62b95216801300442d5cc393c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586270"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>CBaseList.CBaseList(TCHAR, \* INT)-Konstruktor

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

*iItems* 
</dt> <dd>

Größe des Knotencaches.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Zur Effizienz verwaltet `CBaseList` die -Klasse einen Cache von Listenknoten. Wenn Sie ungefähr wissen, wie viele Elemente die Liste enthalten wird, verwenden Sie diese Version des Konstruktors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




