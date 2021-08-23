---
description: Lädt die Daten des Filters aus einem bestimmten Stream.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: CPersistStream.Load-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d65ff2d2ba95f66e6153aa78a9ce376ed144ac24ce8945c1fbc678e9f6894802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813350"
---
# <a name="cpersiststreamload-method"></a>CPersistStream.Load-Methode

Lädt die Daten des Filters aus einem bestimmten Stream.

## <a name="syntax"></a>Syntax


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStm* 
</dt> <dd>

Zeiger auf den Stream, aus dem geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die **IPersistStream::Load-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




