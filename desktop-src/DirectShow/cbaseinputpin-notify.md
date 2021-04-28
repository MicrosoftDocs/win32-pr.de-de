---
description: 'CBaseInputPin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: CBaseInputPin.Notify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119998"
---
# <a name="cbaseinputpinnotify-method"></a>CBaseInputPin.Notify-Methode

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

Zeiger auf den Filter, der die Qualitätskontrollnachricht sendet.

</dd> <dt>

*Q* 
</dt> <dd>

[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Filter übergeben in der Regel Qualitätskontrollmeldungen an einen Upstreamausgabepin, nicht an einen Eingabepin. Daher gibt diese Methode S \_ OK zurück, ohne etwas zu tun.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> <dt>

[Qualitätskontrollverwaltung](quality-control-management.md)
</dt> </dl>

 

 




