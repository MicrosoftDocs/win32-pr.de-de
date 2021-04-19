---
description: Die getpinversion-Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Cbasefilter. getpinversion-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361419"
---
# <a name="cbasefiltergetpinversion-method"></a>Cbasefilter. getpinversion-Methode

Die- `GetPinVersion` Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.

## <a name="syntax"></a>Syntax


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**cbasefilter:: m \_ pinversion**](cbasefilter-m-pinversion.md) -Member-Variable zurück.

## <a name="remarks"></a>Bemerkungen

Der **cbasefilter** -Konstruktor initialisiert die PIN-Version auf 1. In der Basisklasse ändert sich diese Zahl nie. Wenn der Filter Pins dynamisch erstellt oder zerstört, sollte er die PIN-Version erhöhen, wenn die Pins geändert werden. Um die Versionsnummer zu erhöhen, müssen Sie die [**cbasefilter:: incrementpinversion**](cbasefilter-incrementpinversion.md) -Methode aufzurufen.

Das Pin-Enumeratorobjekt, das von der [**cenumpins**](cenumpins.md) -Klasse implementiert wird, verwendet die PIN-Version, um sich selbst mit dem Filter zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




