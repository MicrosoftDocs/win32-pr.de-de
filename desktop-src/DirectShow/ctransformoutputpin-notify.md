---
description: 'CTransformOutputPin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: CTransformOutputPin.Notify-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538140"
---
# <a name="ctransformoutputpinnotify-method"></a>CTransformOutputPin.Notify-Methode

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

[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                       | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Es wurde kein Objekt zum Akzeptieren der Nachricht finden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CTransformFilter::AlterQuality-Methode**](ctransformfilter-alterquality.md) des Filters auf. Wenn der Filter die Qualitätsnachricht nicht verarbeitet, ruft diese Methode die [**CBaseInputPin::P assNotify-Methode**](cbaseinputpin-passnotify.md) auf dem Eingabepin des Filters auf. Die **PassNotify-Methode** übergibt die Qualitätsmeldung upstream (oder an einen benutzerdefinierten Qualitäts-Manager, sofern installiert).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




