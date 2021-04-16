---
description: Die AddAfter-Methode fügt eine Liste nach der angegebenen Position ein und verwendet die Parameter "POS" und "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Cgenericlist. AddAfter-Methode (wxlist. h)-POS, plist-Parameter
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
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531106"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Cgenericlist. AddAfter-Methode (wxlist. h)-POS, plist-Parameter

Die- `AddAfter` Methode fügt eine Liste nach der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Position zum Einfügen der Liste. Die Liste wird nach dieser Position eingefügt.

</dd> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




