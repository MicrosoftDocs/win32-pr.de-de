---
description: Die GetState-Methode ruft den Zustand der Filter ab (wird ausgeführt, angehalten oder angehalten). Diese Methode implementiert die IMediaFilter::GetState-Methode.
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: CBaseFilter.GetState-Methode (Amfilter.h)
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
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017168"
---
# <a name="cbasefiltergetstate-method"></a>CBaseFilter.GetState-Methode

Die `GetState` -Methode ruft den Zustand der Filter ab (wird ausgeführt, angehalten oder angehalten). Diese Methode implementiert die [**IMediaFilter::GetState-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwMsecsTimeout* 
</dt> <dd>

Time out-Intervall in Millisekunden.

</dd> <dt>

*State* 
</dt> <dd>

Zeiger auf eine Variable, die einen Member des Enumerationstyps [**FILTER \_ STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E POINTER \_ zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse sind alle Zustandsübergänge synchron, und der *dwMsecsTimeout-Parameter* wird ignoriert. Wenn eine abgeleitete Klasse asynchrone Zustandsübergänge ausführt, sollte sie diese Methode überschreiben, um während Zustandsübergängen mit einem Timeout von *dwMsecsTimeout* in Millisekunden zu warten.

Wenn Ihr Filter keine Daten übermittelt, während er angehalten wird, überschreiben Sie die `GetState` -Methode, um den Wert VFW \_ S \_ CANT \_ CUE zurückzugeben, wenn der Filter angehalten wird (siehe [Bereitstellen von Beispielen](delivering-samples.md)). Beispiel:


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
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




