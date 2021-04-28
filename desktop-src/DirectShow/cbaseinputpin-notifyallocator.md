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
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099715"
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

Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind. True gibt an, dass Beispiele schreibgeschützt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Während der Stecknadelverbindung wählt der Ausgabepin eine Zuweisung aus und ruft diese Methode auf, um den Eingabepin zu benachrichtigen. Der Ausgabepin kann die Zuweisung verwenden, die der Eingabepin in der [**IMemInputPin::GetAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) vorgeschlagen hat, oder er kann einen eigenen Allocator bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




