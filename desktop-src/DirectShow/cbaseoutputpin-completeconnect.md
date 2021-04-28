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
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099538"
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

Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::CompleteConnect-Methode.**](cbasepin-completeconnect.md) Sie ruft die [**DecideAllocator-Methode**](cbaseoutputpin-decideallocator.md) auf, die die Speicherzuweisung auswählt, die für diese Verbindung verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




