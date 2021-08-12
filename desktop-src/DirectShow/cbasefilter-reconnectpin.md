---
description: Die ReconnectPin-Methode unterbricht eine vorhandene Stecknadelverbindung und verbindet sie unter Verwendung eines angegebenen Medientyps erneut mit demselben Pin.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: CBaseFilter.ReconnectPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39cef0ac5a0a7c4f186b8eae90a96a8e26fbf886f819dc7562cb7d8df4e087e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659720"
---
# <a name="cbasefilterreconnectpin-method"></a>CBaseFilter.ReconnectPin-Methode

Die `ReconnectPin` -Methode unterbricht eine vorhandene Pinverbindung und verbindet sie unter Verwendung eines angegebenen Medientyps erneut mit demselben Pin.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins.

</dd> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp angibt, oder **NULL**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | [**Die \_ m pGraph-Membervariable**](cbasefilter-m-pgraph.md) ist **NULL.**<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**IFilterGraph2::ReconnectEx-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) für den Filtergraph-Manager auf. Wenn die [**IFilterGraph2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) nicht verfügbar ist, ruft die Methode [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




