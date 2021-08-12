---
description: 'CTransInPlaceInputPin.GetAllocator-Methode: Die GetAllocator-Methode ruft die von diesem Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin::GetAllocator-Methode.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: CTransInPlaceInputPin.GetAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c90587cbd0a9cc9b0abed834db68de3edac6f73d98dac3c8bb283e77f978fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654851"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>CTransInPlaceInputPin.GetAllocator-Methode

Die `GetAllocator` -Methode ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab. Diese Methode implementiert die [**IMemInputPin::GetAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                          | Beschreibung                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Es ist keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn der Ausgabepin des Filters verbunden ist, fordert diese Methode eine Zuweisung vom Eingabepin des Downstreamfilters an.

Wenn der Ausgabepin des Filters nicht verbunden ist, erstellt diese Methode eine temporäre Zuweisung. Wenn der Ausgabepin später verbunden ist, verbindet der Filter den Eingabepin erneut und gibt die Zuweisung neu aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceInputPin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




