---
description: Die streamtime-Methode ruft die aktuelle streamzeit ab.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Cbasemediafilter. streamtime-Methode (amfilter. h)
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
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364437"
---
# <a name="cbasemediafilterstreamtime-method"></a>Cbasemediafilter. streamtime-Methode

Die- `StreamTime` Methode ruft die aktuelle streamzeit ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtstream* \[ atur\]
</dt> <dd>

Verweis auf ein-Objekt, das die aktuelle [**streamzeit empfängt**](creftime.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                      | Beschreibung                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Erfolg.<br/>                         |
| <dl> <dt>**VFW \_ E \_ No \_ Clock**</dt> </dl> | Es ist keine Referenzuhr verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die streamzeit wird als aktuelle Bezugszeit (wie durch die verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**cbasemediafilter:: m \_ tSTART**](cbasemediafilter-m-tstart.md)) definiert. Der Zeitstempel eines Medien Beispiels gibt die streamzeit an, zu der er gerendert werden soll. Wenn eine Stichprobe mit einem Zeitstempel, der kleiner ist als die aktuelle streamzeit, noch nicht gerendert wurde, wird Sie später angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




