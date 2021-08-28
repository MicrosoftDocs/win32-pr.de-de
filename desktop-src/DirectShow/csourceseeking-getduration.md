---
description: 'CSourceSeeking.GetDuration-Methode: Die GetDuration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetDuration-Methode.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: CSourceSeeking.GetDuration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8520b39ca62d70152b544e8ae2f146a237c388d93e4786bb13371ad223fa73f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084040"
---
# <a name="csourceseekinggetduration-method"></a>CSourceSeeking.GetDuration-Methode

Die `GetDuration` -Methode ruft die Dauer des Streams ab. Diese Methode implementiert die [**IMediaSeeking::GetDuration-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDuration* 
</dt> <dd>

Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

## <a name="remarks"></a>Hinweise

Die Dauer wird von der [**CSourceSeeking::m \_ rtDuration-Membervariablen**](csourceseeking-m-rtduration.md) angegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




