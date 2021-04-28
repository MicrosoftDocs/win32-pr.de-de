---
description: 'CBaseOutputPin.DeliverBeginFlush-Methode: Die DeliverBeginFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: CBaseOutputPin.DeliverBeginFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099518"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>CBaseOutputPin.DeliverBeginFlush-Methode

Die `DeliverBeginFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Pin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




