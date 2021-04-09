---
description: Erfahren Sie mehr über die Konstruktormethode für cgenericlist. cgenericlist (wxlist. h). Diese Methode verwendet den pName-Parameter.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName-Parameter
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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103870216"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Cgenericlist. cgenericlist-Konstruktor (wxlist. h)-pName-Parameter

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

## <a name="remarks"></a>Bemerkungen

Aus Effizienzgründen verwaltet die- `CGenericList` Klasse einen Cache von Listen Knoten. Für diese Version des Konstruktors wird eine Standard Cache Größe verwendet.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




