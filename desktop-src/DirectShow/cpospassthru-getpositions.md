---
description: 'Die getpositions-Methode ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaseeking:: getpositions-Methode.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Cpospassthru. getpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371205"
---
# <a name="cpospassthrugetpositions-method"></a>Cpospassthru. getpositions-Methode

Die `GetPositions` -Methode ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Position des Stopps in Einheiten des aktuellen Zeit Formats empfängt.

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

 

 




