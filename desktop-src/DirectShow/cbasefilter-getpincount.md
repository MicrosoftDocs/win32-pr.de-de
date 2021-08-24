---
description: 'CBaseFilter.GetPinCount-Methode: Die GetPinCount-Methode ruft die Anzahl der Stecknadeln ab.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: CBaseFilter.GetPinCount-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7d136b5b3bbdcd8a6b21fcbd9f854de7a78a91be87a199c990e294ce8b28fb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640480"
---
# <a name="cbasefiltergetpincount-method"></a>CBaseFilter.GetPinCount-Methode

Die `GetPinCount` -Methode ruft die Anzahl der Stecknadeln ab.

## <a name="syntax"></a>Syntax


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Stecknadeln zurück.

## <a name="remarks"></a>Hinweise

Die abgeleitete Klasse muss diese rein virtuelle Methode implementieren. Gibt die Anzahl der Pins zurück, die derzeit für diesen Filter verfügbar sind. Filter können Pins dynamisch erstellen oder zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




