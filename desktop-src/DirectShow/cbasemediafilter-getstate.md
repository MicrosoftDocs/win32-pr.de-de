---
description: 'Die GetState-Methode ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die imediafilter:: GetState-Methode.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Cbasemediafilter. GetState-Methode (amfilter. h)
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
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352868"
---
# <a name="cbasemediafiltergetstate-method"></a>Cbasemediafilter. GetState-Methode

Die `GetState` -Methode ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwmillisecstimeout* 
</dt> <dd>

Timeout Intervall in Millisekunden.

</dd> <dt>

*State* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse sind alle Zustandsübergänge synchron, und der Parameter " *dwmillisecstimeout* " wird ignoriert. Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte Sie diese Methode überschreiben, um während der Zustandsübergänge zu warten, wobei ein Timeout von *dwmillisecstimeout* -Millisekunden auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




