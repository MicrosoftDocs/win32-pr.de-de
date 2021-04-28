---
description: 'CBaseList.CBaseList-Konstruktor: Konstruktormethode.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: CBaseList.CBaseList-Konstruktor (Wxlist.h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096327"
---
# <a name="cbaselistcbaselist-constructor"></a>CBaseList.CBaseList-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen der Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zur Effizienz verwaltet `CBaseList` die -Klasse einen Cache von Listenknoten. Diese Version des Konstruktors verwendet eine Standardcachegröße.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (streams.h enthalten)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




