---
description: Die ConnectedIMemInputPin-Methode ruft einen Zeiger auf den Downstreameingabepin ab. Diese Methode gibt die Membervariable CBaseOutputPin::m \_ pInputPin zurück.
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: CTransInPlaceOutputPin.ConnectedIMemInputPin-Methode (Transip.h)
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
ms.openlocfilehash: 180cce9bc0d52c6e11bbd90b64cfe7d57d4dcc99eada3a794f924df6857c4698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076180"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>CTransInPlaceOutputPin.ConnectedIMemInputPin-Methode

Die `ConnectedIMemInputPin` -Methode ruft einen Zeiger auf den Downstreameingabepin ab. Diese Methode gibt die [**Membervariable CBaseOutputPin::m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) zurück.

## <a name="syntax"></a>Syntax


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) auf dem Downstreameingabepin zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




