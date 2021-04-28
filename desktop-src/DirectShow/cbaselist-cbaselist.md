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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099638"
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

## <a name="remarks"></a>Bemerkungen

Zur Effizienz verwaltet `CBaseList` die -Klasse einen Cache von Listenknoten. Wenn Sie ungefähr wissen, wie viele Elemente die Liste enthalten wird, verwenden Sie diese Version des Konstruktors.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (streams.h enthalten)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




