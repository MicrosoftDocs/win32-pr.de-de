---
description: 'CBaseOutputPin.EndOfStream-Methode: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die IPin::EndOfStream-Methode.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: CBaseOutputPin.EndOfStream-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096148"
---
# <a name="cbaseoutputpinendofstream-method"></a>CBaseOutputPin.EndOfStream-Methode

Die `EndOfStream` -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt E \_ UNEXPECTED zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte nur für Eingabepins aufgerufen werden, sodass die **CBaseOutputPin-Implementierung** E \_ UNEXPECTED zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




