---
description: Die get \_ CurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die IMediaPosition::get \_ CurrentPosition-Methode.
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: CPosPassThru.get_CurrentPosition -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084240"
---
# <a name="cpospassthruget_currentposition-method"></a>CPosPassThru.get \_ CurrentPosition-Methode

Die `get_CurrentPosition` -Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die [**IMediaPosition::get \_ CurrentPosition-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pllTime* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Position in Sekunden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




