---
description: Die SetSubtype-Methode gibt den Untertyp an.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: CMediaType.SetSubtype-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566370"
---
# <a name="cmediatypesetsubtype-method"></a>CMediaType.SetSubtype-Methode

Die `SetSubtype` -Methode gibt den Untertyp an.

## <a name="syntax"></a>Syntax


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psubtype* 
</dt> <dd>

Zeiger auf eine **GUID,** die den Untertyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




