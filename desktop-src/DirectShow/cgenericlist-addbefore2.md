---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein. Diese Methode verwendet die Parameter "POS" und "plist".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Cgenericlist. AddBefore-Methode (wxlist. h)-POS, plist-Parameter
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
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762423"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Cgenericlist. AddBefore-Methode (wxlist. h)-POS, plist-Parameter

Die- `AddBefore` Methode fügt eine Liste vor der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Position zum Einfügen der Liste. Die Liste wird vor dieser Position eingefügt.

</dd> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




