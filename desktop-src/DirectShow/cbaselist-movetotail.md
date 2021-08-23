---
description: Die MoveToTail-Methode teilt die Liste und fügt den Hauptteil an das Ende einer anderen Liste an.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: CBaseList.MoveToTail-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae7ab918c8c4ef707b2754f8b1ba1f8f3e76265a6b8ac0b252e765de2aff1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016918"
---
# <a name="cbaselistmovetotail-method"></a>CBaseList.MoveToTail-Methode

Die `MoveToTail` -Methode teilt die Liste auf und fügt den Hauptteil an das Ende einer anderen Liste an.

## <a name="syntax"></a>Syntax


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionsindikator, der die Teilung in der Liste markiert.

</dd> <dt>

*Plist* 
</dt> <dd>

Zeiger auf eine andere Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode teilt die Liste nach der durch den pos-Parameter *angegebenen Position* auf. Der Abschnitt tail verbleibt in der Liste. Der Hauptteil wird an das Ende der anderen Liste angefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




