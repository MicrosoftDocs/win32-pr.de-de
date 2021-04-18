---
description: 'Die getduration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die imediaseeking:: getduration-Methode.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Csourceseeking. getduration-Methode (ctlutil. h)
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
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354646"
---
# <a name="csourceseekinggetduration-method"></a>Csourceseeking. getduration-Methode

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

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Dauer wird von der [**csourceseeking:: m \_ rtduration**](csourceseeking-m-rtduration.md) -Element Variablen angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




