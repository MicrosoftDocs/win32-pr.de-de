---
description: Die Methode "muvedetail" teilt die Liste und fügt Sie an das Ende einer anderen Liste an.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Cbaselist. muvedetail-Methode (wxlist. h)
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
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370115"
---
# <a name="cbaselistmovetotail-method"></a>Cbaselist. muvedetail-Methode

Die `MoveToTail` -Methode teilt die Liste auf und fügt Sie an das Ende einer anderen Liste an.

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

Positionsindikator, mit dem die Aufteilung in der Liste markiert wird.

</dd> <dt>

*pList* 
</dt> <dd>

Zeiger auf eine andere Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode teilt die Liste nach der durch den *POS* -Parameter angegebenen Position. Der Teil Fragment verbleibt in der Liste. Der Kopfteil wird an das Ende der anderen Liste angehängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




