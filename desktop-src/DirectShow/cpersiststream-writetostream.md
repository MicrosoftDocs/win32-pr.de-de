---
description: Schreibt die Daten des Filters in den angegebenen Stream.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: CPersistStream.WriteToStream-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 139818d1434163255c62dd5cb109dbf505cea03b5876de14eb2aa4a0636f072f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813290"
---
# <a name="cpersiststreamwritetostream-method"></a>CPersistStream.WriteToStream-Methode

Schreibt die Daten des Filters in den angegebenen Stream.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStream* 
</dt> <dd>

Zeiger auf eine **IStream-Schnittstelle,** die den Zielstream der Filterdaten angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück. Die abgeleitete Klasse sollte einen gültigen **HRESULT-Wert** zurückgeben.

## <a name="remarks"></a>Hinweise

Die Standardversion schreibt nichts. sie kann überschrieben werden, um datenspezifisch für Ihre Klasse zu schreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




