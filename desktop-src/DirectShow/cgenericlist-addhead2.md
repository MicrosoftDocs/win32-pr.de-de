---
description: Die AddHead-Methode fügt am Ende der Liste eine Liste hinzu.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: CGenericList.AddHead-Methode (Wxlist.h) – pList-Parameter
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
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656146"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>CGenericList.AddHead-Methode (Wxlist.h) – pList-Parameter

Die `AddHead` -Methode fügt am Ende der Liste eine Liste hinzu.

## <a name="syntax"></a>Syntax


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plist* 
</dt> <dd>

Zeiger auf die Liste der hinzuzufügende Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




