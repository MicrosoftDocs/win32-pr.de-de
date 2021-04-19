---
description: Liest die Filterdaten aus dem angegebenen Stream.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Cpersiststream. Read FromStream-Methode (pStream. h)
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
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361295"
---
# <a name="cpersiststreamreadfromstream-method"></a>Cpersiststream. Read FromStream-Methode

Liest die Filterdaten aus dem angegebenen Stream.

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

Zeiger auf eine **IStream** -Schnittstelle, aus der Daten gelesen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück. Die abgeleitete Klasse sollte einen gültigen **HRESULT** -Wert zurückgeben.

## <a name="remarks"></a>Bemerkungen

Die Standardversion liest nichts. Sie kann überschrieben werden, um Daten zu lesen, die für Ihre Klasse spezifisch sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




