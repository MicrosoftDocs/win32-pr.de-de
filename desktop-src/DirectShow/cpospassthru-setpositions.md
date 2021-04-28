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
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085478"
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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




