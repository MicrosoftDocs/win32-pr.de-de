---
description: 'Die Checkfunktionen-Methode fragt ab, ob der Stream Suchfunktionen angegeben hat. Diese Methode implementiert die imediaseeking:: Checkfunktionen-Methode.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Csourceseeking. Checkfunktionen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358280"
---
# <a name="csourceseekingcheckcapabilities-method"></a>Csourceseeking. checksources-Methode

Die- `CheckCapabilities` Methode fragt ab, ob der Stream Suchfunktionen angegeben hat. Diese Methode implementiert die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunktionen* 
</dt> <dd>

Zeiger auf eine bitweise Kombination von einem oder mehreren Suchfunktionen, die [**\_ \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) suchen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Nicht alle Funktionen in *pfunktionen* sind vorhanden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Alle Funktionen in *pfunktionen* sind vorhanden.<br/>            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/>                                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überprüft den Wert von *\* psources* anhand der Element Variablen [**csourceseeking:: m \_ dwseekingcaps**](csourceseeking-m-dwseekingcaps.md) , wie implementiert. *\* P-Funktionen* werden jedoch nicht gleich **m \_ dwseekingcaps** festgelegt, wie für die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode beschrieben. Auch wenn keine der angegebenen Funktionen verfügbar ist, gibt die Methode E Fail nicht zurück \_ . Eine umfassendere Implementierung sieht wie folgt aus:


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




