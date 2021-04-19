---
description: 'Die getduration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die imediaseeking:: getduration-Methode.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Cpospassthru. getduration-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361275"
---
# <a name="cpospassthrugetduration-method"></a>Cpospassthru. getduration-Methode

Die- `GetDuration` Methode ruft die Dauer des Streams ab. Diese Methode implementiert die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pduration* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeit Formats empfängt.

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

 

 




