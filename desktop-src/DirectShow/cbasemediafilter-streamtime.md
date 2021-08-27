---
description: 'CBaseMediaFilter.StreamTime-Methode: Die StreamTime-Methode ruft die aktuelle Streamzeit ab.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: CBaseMediaFilter.StreamTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99205cb7065b7bd57d0f49a7f4942df8c1548ba5d4b4f8b26c8a13387ddc7d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076590"
---
# <a name="cbasemediafilterstreamtime-method"></a>CBaseMediaFilter.StreamTime-Methode

Die `StreamTime` -Methode ruft die aktuelle Streamzeit ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Verweis auf ein [**CRefTime-Objekt,**](creftime.md) das die aktuelle Streamzeit empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                      | Beschreibung                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Erfolg.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | Es ist keine Referenzuhr verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Streamzeit wird als die aktuelle Referenzzeit (wie durch die Verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)) definiert. Der Zeitstempel eines Medienbeispiels gibt die Streamzeit an, zu der es gerendert werden soll. Wenn ein Beispiel mit einem Zeitstempel kleiner als die aktuelle Streamzeit noch nicht gerendert wurde, kommt es zu einem späteren Zeitpunkt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




