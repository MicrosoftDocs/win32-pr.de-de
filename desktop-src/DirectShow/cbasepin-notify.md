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
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096018"
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

Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Filters, der die Qualitätskontrollmeldung übermittelt hat.

</dd> <dt>

*Q* 
</dt> <dd>

Gibt eine [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) an, die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklasse gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Bemerkungen

Ausgabepins sollten diese Methode überschreiben, um Qualitätskontrollmeldungen zu akzeptieren.

Wenn ein externer Qualitäts-Manager installiert wurde (siehe [**CBasePin::SetSink),**](cbasepin-setsink.md)übergeben Sie die Nachricht an diesen Qualitäts-Manager. Andernfalls sollte der Filter die Nachricht selbst verarbeiten oder die Nachricht upstream übergeben. Weitere Informationen finden Sie unter [Qualitätskontrollverwaltung.](quality-control-management.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




