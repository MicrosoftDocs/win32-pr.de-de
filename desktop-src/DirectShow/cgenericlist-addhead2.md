---
description: Mit der AddHead-Methode wird eine Liste am Anfang der Liste hinzugefügt.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Cgenericlist. AddHead-Methode (wxlist. h)-plist-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106367407"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Cgenericlist. AddHead-Methode (wxlist. h)-plist-Parameter

Mit der- `AddHead` Methode wird eine Liste am Anfang der Liste hinzugefügt.

## <a name="syntax"></a>Syntax


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die Liste der hinzu zufügenden Elemente.

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

 

 




