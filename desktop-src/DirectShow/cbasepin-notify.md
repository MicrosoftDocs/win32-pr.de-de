---
description: 'CBasePin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: CBasePin.Notify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910440"
---
# <a name="cbasepinnotify-method"></a>CBasePin.Notify-Methode

Die `Notify` -Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die [**IQualityControl::Notify-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSelf* 
</dt> <dd>

Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Filters, der die Qualitätskontrollnachricht übermittelt hat.

</dd> <dt>

*Q* 
</dt> <dd>

Gibt eine [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) an, die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklasse gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Ausgabepins sollten diese Methode überschreiben, um Qualitätskontrollmeldungen zu akzeptieren.

Wenn ein externer Qualitäts-Manager installiert wurde (siehe [**CBasePin::SetSink**](cbasepin-setsink.md)), übergeben Sie die Nachricht an diesen Qualitäts-Manager. Andernfalls sollte der Filter die Nachricht selbst verarbeiten oder die Nachricht upstream übergeben. Weitere Informationen finden Sie unter [Quality-Control Management](quality-control-management.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




