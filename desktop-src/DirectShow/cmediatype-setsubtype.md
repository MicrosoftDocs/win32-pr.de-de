---
description: Die setsubtype-Methode gibt den Untertyp an.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Cmediatype. setsubtype-Methode (mtype. h)
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
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352949"
---
# <a name="cmediatypesetsubtype-method"></a>Cmediatype. setsubtype-Methode

Die- `SetSubtype` Methode gibt den Untertyp an.

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

Zeiger auf eine **GUID** , die den Untertyp angibt.

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

 

 




