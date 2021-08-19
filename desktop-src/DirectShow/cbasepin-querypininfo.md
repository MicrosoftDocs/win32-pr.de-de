---
description: Die QueryPinInfo-Methode ruft Informationen zum Pin ab. Diese Methode implementiert die IPin::QueryPinInfo-Methode.
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: CBasePin.QueryPinInfo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823232"
---
# <a name="cbasepinquerypininfo-method"></a>CBasePin.QueryPinInfo-Methode

Die `QueryPinInfo` -Methode ruft Informationen zum Pin ab. Diese Methode implementiert die [**IPin::QueryPinInfo-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pinfo* 
</dt> <dd>

Zeiger auf eine [**\_ PIN-INFO-Struktur,**](/windows/win32/api/strmif/ns-strmif-pin_info) die die Pininformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="remarks"></a>Hinweise

Diese Methode verwendet die [**CBasePin::m \_ pName-Membervariable**](cbasepin-m-pname.md) für das **Member "pinName"** der PIN \_ INFO-Struktur.

Wenn die Methode zurückgibt und das **pFilter-Member** der PIN INFO-Struktur nicht NULL ist, verfügt sie \_ über eine ausstehendeVerweisanzahl. Stellen Sie sicher, dass Sie die Schnittstelle wieder frei geben, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




