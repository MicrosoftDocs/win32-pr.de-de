---
description: Die displaytypeinfo-Methode zeigt während des Debuggens Medientyp Informationen an.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Cbasepin. displaytypeinfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361557"
---
# <a name="cbasepindisplaytypeinfo-method"></a>Cbasepin. displaytypeinfo-Methode

Die- `DisplayTypeInfo` Methode zeigt während des Debuggens Medientyp Informationen an.

## <a name="syntax"></a>Syntax


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In Debugbuilds ruft diese Methode die [**dbglog**](dbglog.md) -Funktion auf, um den angegebenen Medientyp anzuzeigen. Bei Einzelhandels Builds führt diese Methode keine Aktion aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




