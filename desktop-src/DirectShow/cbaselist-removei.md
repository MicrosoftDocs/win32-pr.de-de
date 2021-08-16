---
description: Die RemoveI-Methode entfernt das Element an der angegebenen Position.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: CBaseList.RemoveI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac3277f30e959e42cf2fd2d1aeeb13f81cb17515abb8434a8ae13406d244aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823737"
---
# <a name="cbaselistremovei-method"></a>CBaseList.RemoveI-Methode

Die `RemoveI` -Methode entfernt das Element an der angegebenen Position.

## <a name="syntax"></a>Syntax


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

POSITION-Wert, der das zu entfernende Element angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löscht den Knoten aus der Liste, aber nicht das in diesem Knoten enthaltene Element.

Wenn *pos* **NULL** ist, gibt die Methode **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




