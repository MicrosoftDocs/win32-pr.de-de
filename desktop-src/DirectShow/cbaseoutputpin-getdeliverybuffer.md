---
description: Die getdeliverybuffer-Methode ruft ein Medien Beispiel ab, das einen leeren Puffer enthält.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Cbaseoutputpin. getdeliverybuffer-Methode (amfilter. h)
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
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373953"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Cbaseoutputpin. getdeliverybuffer-Methode

Die- `GetDeliveryBuffer` Methode ruft ein Medien Beispiel ab, das einen leeren Puffer enthält.

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

*ppsample* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Puffers empfängt.

</dd> <dt>

*pstarttime* 
</dt> <dd>

Ein Zeiger auf die Startzeit des Beispiels oder **null**.

</dd> <dt>

*Zeit* 
</dt> <dd>

Ein Zeiger auf die Endzeit der Stichprobe oder **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Bitweise Kombination von Flags, die von der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Schnittstelle unterstützt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die **imemzuzucator:: GetBuffer** -Methode für die Zuweisung auf und übergibt die Parameter an diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




