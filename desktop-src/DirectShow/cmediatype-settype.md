---
description: Die settype-Methode gibt den Haupttyp an.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Cmediatype. SetType-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371301"
---
# <a name="cmediatypesettype-method"></a>Cmediatype. SetType-Methode

Die- `SetType` Methode gibt den Haupttyp an.

## <a name="syntax"></a>Syntax


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pType* 
</dt> <dd>

Zeiger auf eine **GUID** , die den Haupttyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




