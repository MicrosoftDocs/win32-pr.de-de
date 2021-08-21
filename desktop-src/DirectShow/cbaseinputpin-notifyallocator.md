---
description: 'CBaseInputPin.NotifyAllocator-Methode: Die NotifyAllocator-Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die IMemInputPin::NotifyAllocator-Methode.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: CBaseInputPin.NotifyAllocator-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37bcd7d8d69f18dce98339a34a4641ddd2502e946e29a0097fe6c381f4af5c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017008"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>CBaseInputPin.NotifyAllocator-Methode

Die `NotifyAllocator` -Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die [**IMemInputPin::NotifyAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAllocator* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Flag, das angibt, ob Stichproben aus dieser Zuweisung schreibgeschützt sind. True gibt an, dass Beispiele schreibgeschützt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Während der Pinverbindung wählt der Ausgabepin eine Zuweisung aus und ruft diese Methode auf, um den Eingabepin zu benachrichtigen. Der Ausgabepin kann die Zuweisung verwenden, die der Eingabepin in der [**IMemInputPin::GetAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) vorgeschlagen hat, oder er kann einen eigenen Allocator bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




