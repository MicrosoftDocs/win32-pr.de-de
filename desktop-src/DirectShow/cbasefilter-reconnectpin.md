---
description: Die reconnectpin-Methode unterbricht eine vorhandene Pin-Verbindung und verbindet Sie mit dem gleichen PIN, wobei ein angegebener Medientyp verwendet wird.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Cbasefilter. reconnectpin-Methode (amfilter. h)
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
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369525"
---
# <a name="cbasefilterreconnectpin-method"></a>Cbasefilter. reconnectpin-Methode

Die `ReconnectPin` -Methode unterbricht eine vorhandene Pin-Verbindung und verbindet Sie mit dem gleichen PIN, wobei ein angegebener Medientyp verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Ein Zeiger auf eine [**am- \_ Medientyp \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt, oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                               |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | die [**m- \_ PGraph**](cbasefilter-m-pgraph.md) -Element Variable ist **null**.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IFilterGraph2:: reconnectex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) -Methode für den Filter Graph-Manager auf. Wenn die [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) -Schnittstelle nicht verfügbar ist, ruft die-Methode [**ifiltergraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




