---
description: Die AddAfter-Methode fügt eine Liste nach der angegebenen Position ein und verwendet die Parameter "pos" und "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: CGenericList.AddAfter-Methode (Wxlist.h) – pos, plist-Parameter
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
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697480"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>CGenericList.AddAfter-Methode (Wxlist.h) – pos, plist-Parameter

Die `AddAfter` -Methode fügt eine Liste nach der angegebenen Position ein.

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

*Plist* 
</dt> <dd>

Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




