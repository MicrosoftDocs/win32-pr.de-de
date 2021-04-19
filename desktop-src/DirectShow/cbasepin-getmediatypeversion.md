---
description: Die getmediatypeer Version-Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Cbasepin. getmediatypeer Version-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371565"
---
# <a name="cbasepingetmediatypeversion-method"></a>Cbasepin. getmediatypeer Version-Methode

Die- `GetMediaTypeVersion` Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.

## <a name="syntax"></a>Syntax


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**cbasepin:: m \_ typeversion**](cbasepin-m-typeversion.md) -Member-Variable zurück.

## <a name="remarks"></a>Bemerkungen

Der **cbasepin** -Konstruktor initialisiert die Versionsnummer auf 1. In der Basisklasse ändert sich diese Zahl nie. Wenn die PIN die Liste der bevorzugten Medientypen dynamisch ändert, sollte Sie die Versionsnummer erhöhen, wenn die Liste geändert wird. Um die Versionsnummer zu erhöhen, müssen Sie die [**cbasepin:: incrementtypeversion**](cbasepin-incrementtypeversion.md) -Methode aufzurufen.

Der Medientyp Enumerator, der von der [**cenummediatypes**](cenummediatypes.md) -Klasse implementiert wird, verwendet die Versionsnummer, um sich selbst mit der PIN zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




