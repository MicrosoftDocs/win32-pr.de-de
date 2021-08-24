---
description: Die GetState-Methode ruft den Zustand des Objekts ab (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die IMediaFilter::GetState-Methode.
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: CBaseMediaFilter.GetState-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966700"
---
# <a name="cbasemediafiltergetstate-method"></a>CBaseMediaFilter.GetState-Methode

Die `GetState` -Methode ruft den Zustand des Objekts ab (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die [**IMediaFilter::GetState-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Time out interval ,in milliseconds. (Time out interval in milliseconds(Time out-Intervall in Millisekunden))

</dd> <dt>

*State* 
</dt> <dd>

Zeiger auf eine Variable, die einen Member des aufzählten [**FILTER \_ STATE-Typs**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse sind alle Zustandsübergänge synchron, und der *dwMilliSecsTimeout-Parameter* wird ignoriert. Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte sie diese Methode überschreiben, um während Zustandsübergängen mit einem Timeout von *dwMilliSecsTimeout* Millisekunden zu warten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




