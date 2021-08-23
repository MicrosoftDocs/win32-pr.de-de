---
description: 'CRenderedInputPin.CRenderedInputPin-Konstruktor : Konstruktormethode.'
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: CRenderedInputPin.CRenderedInputPin-Konstruktor (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b75ce6b5f91f5bd9019a4bf6e46266269b72ac7a5e719f7a58b2f2e702375a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953829"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a>CRenderedInputPin.CRenderedInputPin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CRenderedInputPin(
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

Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject-Klasse.**](cbaseobject.md)

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRenderedInputPin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




