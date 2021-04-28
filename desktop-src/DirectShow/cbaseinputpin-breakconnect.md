---
description: 'CBaseInputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: CBaseInputPin.BreakConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099738"
---
# <a name="cbaseinputpinbreakconnect-method"></a>CBaseInputPin.BreakConnect-Methode

Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::BreakConnect-Methode.**](cbasepin-breakconnect.md) Er dekommitiert die Zuweisung und gibt die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) frei.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus Ihrer überschreibenden Methode auf. Andernfalls können Speicherverluste entstehen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




