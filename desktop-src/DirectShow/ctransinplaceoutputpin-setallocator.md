---
description: Die SetAllocator-Methode gibt eine Zuweisung für die Verbindung an.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: CTransInPlaceOutputPin.SetAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 568a95df0d0cee39245c268fa1c49505531ddc84e1fd1542a1eae170e5c7d0da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053180"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>CTransInPlaceOutputPin.SetAllocator-Methode

Die `SetAllocator` -Methode gibt eine Zuweisung für die Verbindung an.

## <a name="syntax"></a>Syntax


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAllocator* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle der Zuweisung.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Ausgabepin für diesen Filter stellt nie eine Zuweisung zurVerfingung zurVerfingung. Diese Methode gibt die Zuweisung für den Ausgabepin an. Er legt den Wert der [**CBaseOutputPin::m \_ pAllocator-Membervariable**](cbaseoutputpin-m-pallocator.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




