---
description: Die deliverendflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Cbaseoutputpin. deliverendflush-Methode (amfilter. h)
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
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371729"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>Cbaseoutputpin. deliverendflush-Methode

Die- `DeliverEndFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




