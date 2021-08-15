---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein. Diese Methode verwendet die Parameter "pos" und "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: CGenericList.AddBefore-Methode (Wxlist.h) – pos, pList-Parameter
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
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697450"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>CGenericList.AddBefore-Methode (Wxlist.h) – pos, pList-Parameter

Die `AddBefore` -Methode fügt eine Liste vor der angegebenen Position ein.

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

*Plist* 
</dt> <dd>

Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich. Andernfalls gibt **FALSE** zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




