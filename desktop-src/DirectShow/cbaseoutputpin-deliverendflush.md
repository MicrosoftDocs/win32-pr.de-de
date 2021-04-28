---
description: 'CBaseOutputPin.DeliverEndFlush-Methode: Die DeliverEndFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.'
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: CBaseOutputPin.DeliverEndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096178"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>CBaseOutputPin.DeliverEndFlush-Methode

Die `DeliverEndFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Die Stecknadel ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für den Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




