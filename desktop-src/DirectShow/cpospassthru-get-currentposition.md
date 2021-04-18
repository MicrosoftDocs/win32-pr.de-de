---
description: 'Die get \_ CurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaposition:: get \_ CurrentPosition-Methode.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: CPosPassThru.get_CurrentPosition-Methode (ctlutil. h)
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
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368501"
---
# <a name="cpospassthruget_currentposition-method"></a>Cpospassthru. get \_ CurrentPosition-Methode

Die- `get_CurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die [**imediaposition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plltime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position (in Sekunden) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




