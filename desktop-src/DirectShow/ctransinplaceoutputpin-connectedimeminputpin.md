---
description: 'Die connectedimeminputpin-Methode ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab. Diese Methode gibt die cbaseoutputpin:: m \_ pinputpin-Member-Variable zurück.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Ctransinplaceoutputpin. connectedimeminputpin-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357595"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>Ctransinplaceoutputpin. connectedimeminputpin-Methode

Die- `ConnectedIMemInputPin` Methode ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab. Diese Methode gibt die [**cbaseoutputpin:: m \_ pinputpin**](cbaseoutputpin-m-pinputpin.md) -Member-Variable zurück.

## <a name="syntax"></a>Syntax


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle der nachgeschalteten Eingabe-PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceoutputpin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




