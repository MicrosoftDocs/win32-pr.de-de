---
description: 'CBaseOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem Eingabepin ab.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: CBaseOutputPin.CompleteConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9832ddc0a68936461f9fe9ee8a70a7da3227f93e9b0bc9f7328d4cc2f95c2f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823670"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>CBaseOutputPin.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Verbindung mit einem Eingabepin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf den Eingabepin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::CompleteConnect-Methode.**](cbasepin-completeconnect.md) Sie ruft die [**DecideAllocator-Methode**](cbaseoutputpin-decideallocator.md) auf, die die Speicherzuweisung auswählt, die für diese Verbindung verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




