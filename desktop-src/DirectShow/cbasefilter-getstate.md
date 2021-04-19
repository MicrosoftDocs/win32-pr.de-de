---
description: 'Mit der GetState-Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die imediafilter:: GetState-Methode.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Cbasefilter. GetState-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370754"
---
# <a name="cbasefiltergetstate-method"></a>Cbasefilter. GetState-Methode

Mit der `GetState` -Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten). Diese Methode implementiert die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode.

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

Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse sind alle Zustandsübergänge synchron, und der Parameter " *dwmillisecstimeout* " wird ignoriert. Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte Sie diese Methode überschreiben, um während der Zustandsübergänge zu warten, wobei ein Timeout von *dwmillisecstimeout* -Millisekunden auftritt.

Wenn der Filter keine Daten bereitstellt, während Sie angehalten werden, überschreiben Sie die- `GetState` Methode, um den Wert von VFW S nicht zu senden, \_ \_ \_ Wenn der Filter angehalten wird (siehe [Bereitstellung von Beispielen](delivering-samples.md)). Beispiel:


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




