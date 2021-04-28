---
description: CBaseOutputPin.CBaseOutputPin-Konstruktor – Konstruktormethode.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: CBaseOutputPin.CBaseOutputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9901591be32d431ebe53a2098456446a0126d26b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099568"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>CBaseOutputPin.CBaseOutputPin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diese Stecknadel erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird. Dies kann derselbe kritische Abschnitt wie die Filtersperre [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md)sein.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Pinnamen enthält (wird auch als Stecknadelbezeichner verwendet).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle Parameter werden direkt an den [**CBasePin-Konstruktor**](cbasepin.md) übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




