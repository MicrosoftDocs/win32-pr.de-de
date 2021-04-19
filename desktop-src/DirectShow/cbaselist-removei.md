---
description: Die removei-Methode entfernt das Element an der angegebenen Position.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Cbaselist. removei-Methode (wxlist. h)
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
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365701"
---
# <a name="cbaselistremovei-method"></a>Cbaselist. removei-Methode

Die- `RemoveI` Methode entfernt das Element an der angegebenen Position.

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

Positionswert, der das zu entfern gende Element angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Knoten aus der Liste, löscht jedoch nicht das Element, das in diesem Knoten enthalten ist.

Wenn *POS* **null** ist, gibt die Methode **null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




