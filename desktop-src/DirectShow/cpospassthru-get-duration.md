---
description: Die \_ Get Duration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaPosition::get \_ Duration-Methode.
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: CPosPassThru.get_Duration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e39dadd5a652b7b88321f21f1d5312c1ac44a1f1f23e7be75f9aab3460938aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915480"
---
# <a name="cpospassthruget_duration-method"></a>CPosPassThru.get \_ Duration-Methode

Die `get_Duration` -Methode ruft die Dauer des Streams ab. Diese Methode implementiert die [**IMediaPosition::get \_ Duration-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ngth* 
</dt> <dd>

Zeiger auf eine Variable, die die gesamte Streamlänge in Sekunden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




