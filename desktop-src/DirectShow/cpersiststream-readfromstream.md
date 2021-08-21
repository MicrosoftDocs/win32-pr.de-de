---
description: Liest die Daten des Filters aus dem angegebenen Stream.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: CPersistStream.ReadFromStream-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073644"
---
# <a name="cpersiststreamreadfromstream-method"></a>CPersistStream.ReadFromStream-Methode

Liest die Daten des Filters aus dem angegebenen Stream.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStream* 
</dt> <dd>

Zeiger auf eine **IStream-Schnittstelle,** aus der Daten gelesen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück. Die abgeleitete Klasse sollte einen gültigen **HRESULT-Wert** zurückgeben.

## <a name="remarks"></a>Hinweise

Die Standardversion liest nichts. kann überschrieben werden, um klassenspezifische Daten zu lesen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




