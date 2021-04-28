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
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096248"
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



 

## <a name="remarks"></a>Bemerkungen

Die Streamzeit wird als aktuelle Referenzzeit (wie von der Referenzuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)) definiert. Der Zeitstempel eines Medienbeispiels gibt die Streamzeit an, zu der es gerendert werden soll. Wenn ein Beispiel mit einem Zeitstempel, der kleiner als die aktuelle Streamzeit ist, noch nicht gerendert wurde, ist es zu spät.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




