---
description: 'CBaseInputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin aus einer Verbindung frei.'
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
ms.openlocfilehash: 625eab8cc070240d79456bff919317f884826fc6d14c26055b68de40aba4c969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403489"
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

Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::BreakConnect-Methode.**](cbasepin-breakconnect.md) Er decommitiert die Zuweisung und gibt die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) frei.

Wenn Sie diese Methode überschreiben, rufen Sie die Basisklassenmethode aus ihrer überschreibenden Methode auf. Andernfalls können Speicherverlusten verursacht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




