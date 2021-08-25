---
description: 'CPosPassThru.SetPositions-Methode: Die SetPositions-Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die IMediaSeeking::SetPositions-Methode.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: CPosPassThru.SetPositions-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d5ed5a25c5ceb4cbe96571ef83945fdf5edd1bbd373de875f7339c13c1b43dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909190"
---
# <a name="cpospassthrusetpositions-method"></a>CPosPassThru.SetPositions-Methode

Die `SetPositions` -Methode legt die aktuelle Position und die Stoppposition fest. Diese Methode implementiert die [**IMediaSeeking::SetPositions-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCurrent* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeitformats angibt.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Bitweise Kombination von Flags. Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Beendigungszeit in Einheiten des aktuellen Zeitformats angibt.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Bitweise Kombination von Flags. Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




