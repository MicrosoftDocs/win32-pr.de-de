---
description: Die GetDeliveryBuffer-Methode ruft ein Medienbeispiel ab, das einen leeren Puffer enthält.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: CBaseOutputPin.GetDeliveryBuffer-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823609"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>CBaseOutputPin.GetDeliveryBuffer-Methode

Die `GetDeliveryBuffer` -Methode ruft ein Medienbeispiel ab, das einen leeren Puffer enthält.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSample* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Puffers empfängt.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf die Startzeit des Beispiels oder **NULL.**

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf die Endzeit des Beispiels oder **NULL.**

</dd> <dt>

*dwFlags* 
</dt> <dd>

Bitweise Kombination von Flags, die von der [**IMemAllocator::GetBuffer-Schnittstelle unterstützt**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die **IMemAllocator::GetBuffer-Methode** für die Zuweisung auf und übergibt die Parameter an diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




