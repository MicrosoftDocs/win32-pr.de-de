---
description: Die PassNotify-Methode übergibt eine Qualitätskontrollmeldung an das entsprechende Objekt.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: CBaseInputPin.PassNotify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760ec066a9d4876dd6ef754783c41ae12765db10c1595d08aef0a73258de087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016998"
---
# <a name="cbaseinputpinpassnotify-method"></a>CBaseInputPin.PassNotify-Methode

Die `PassNotify` -Methode übergibt eine Qualitätskontrollmeldung an das entsprechende -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Q* 
</dt> <dd>

[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                       | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Es wurde kein Objekt zum Akzeptieren der Nachricht finden.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, wenn der Filter keine Qualitätskontrollmeldungen verarbeitet. Diese Methode übergibt die Nachricht in der bevorzugten Reihenfolge an eines der folgenden Objekte:

-   Ein externer Qualitätskontroll-Manager, wenn die [**IQualityControl::SetSink-Methode**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) aufgerufen wurde.
-   Der Upstreamausgabepin.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> <dt>

[Qualitätskontrollverwaltung](quality-control-management.md)
</dt> </dl>

 

 




