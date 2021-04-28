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
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099788"
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

## <a name="remarks"></a>Bemerkungen

Die abgeleitete Klasse muss diese rein virtuelle Methode implementieren. Gibt die Anzahl der Pins zurück, die derzeit für diesen Filter verfügbar sind. Filter können Pins dynamisch erstellen oder zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




