---
description: Erfahren Sie mehr über die Konstruktormethode für CGenericList.CGenericList (Wxlist.h). Diese Methode verwendet den Parameter "pName".
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: CGenericList.CGenericList-Konstruktor (Wxlist.h) – pName-Parameter
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
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813840"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>CGenericList.CGenericList-Konstruktor (Wxlist.h) – pName-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen der Liste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Aus Effizienzgründen verwaltet die `CGenericList` -Klasse einen Cache mit Listenknoten. Diese Version des Konstruktors verwendet eine Standardcachegröße.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




