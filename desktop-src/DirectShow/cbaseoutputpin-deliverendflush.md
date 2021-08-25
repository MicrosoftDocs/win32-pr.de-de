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
ms.openlocfilehash: 6225406d23dd409c9d2b1ff3dcb7669fa468d8f8cba6c49773dbe057c4545cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076565"
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



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für den Eingabepin auf.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




