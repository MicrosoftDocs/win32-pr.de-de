---
description: Die GetMediaTypeVersion-Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: CBasePin.GetMediaTypeVersion-Methode (Amfilter.h)
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
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955189"
---
# <a name="cbasepingetmediatypeversion-method"></a>CBasePin.GetMediaTypeVersion-Methode

Die `GetMediaTypeVersion` -Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.

## <a name="syntax"></a>Syntax


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBasePin::m \_ TypeVersion-Membervariable**](cbasepin-m-typeversion.md) zurück.

## <a name="remarks"></a>Hinweise

Der **CBasePin-Konstruktor** initialisiert die Versionsnummer mit 1. In der Basisklasse ändert sich diese Zahl nie. Wenn der Pin die Liste der bevorzugten Medientypen dynamisch ändert, sollte die Versionsnummer bei jeder Änderung der Liste erhöht werden. Um die Versionsnummer zu erhöhen, rufen Sie die [**CBasePin::IncrementTypeVersion-Methode**](cbasepin-incrementtypeversion.md) auf.

Der Medientyp-Enumerator, der von der [**CEnumMediaTypes-Klasse**](cenummediatypes.md) implementiert wird, verwendet die Versionsnummer, um sich selbst mit dem Pin zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




