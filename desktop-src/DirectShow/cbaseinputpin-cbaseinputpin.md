---
description: 'CBaseInputPin.CBaseInputPin-Konstruktor : Konstruktormethode.'
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: CBaseInputPin.CBaseInputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 526c10dc0cda2f9b4d4cee6a955620f2aa1aae697522aaf3e14e57c3317ca325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017068"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a>CBaseInputPin.CBaseInputPin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird. Dies kann derselbe kritische Abschnitt wie die Filtersperre [**CBaseFilter::m \_ pLock sein.**](cbasefilter-m-plock.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.

</dd> <dt>

*pPinName* 
</dt> <dd>

Breitzeichenfolge mit dem Pinnamen (wird auch als Pinbezeichner verwendet).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle Parameter werden direkt an den [**CBasePin-Konstruktor**](cbasepin-cbasepin.md) übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




