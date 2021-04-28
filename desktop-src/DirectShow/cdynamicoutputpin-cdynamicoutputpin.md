---
description: CDynamicOutputPin.CDynamicOutputPin-Konstruktor – Konstruktormethode.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: CDynamicOutputPin.CDynamicOutputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099308"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>CDynamicOutputPin.CDynamicOutputPin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CDynamicOutputPin(
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

Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird. Verwenden Sie den gleichen kritischen Abschnitt wie die Filtersperre [ **CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Breitzeichenzeichenfolge, die den Pinbezeichner enthält. Weitere Informationen finden Sie unter [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




