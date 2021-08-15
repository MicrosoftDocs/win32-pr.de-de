---
description: Die SetType-Methode gibt den Haupttyp an.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: CMediaType.SetType-Methode (Mtype.h)
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
ms.openlocfilehash: 37d035202d4674da11016620dc3c3d1ba3ab99f6ca514b9581f7dd2e4d9592d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954389"
---
# <a name="cmediatypesettype-method"></a>CMediaType.SetType-Methode

Die `SetType` -Methode gibt den Haupttyp an.

## <a name="syntax"></a>Syntax


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptype* 
</dt> <dd>

Zeiger auf eine **GUID,** die den Haupttyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




