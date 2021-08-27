---
description: Die GetStopPosition-Methode ruft den Zeitpunkt ab, zu dem die Wiedergabe relativ zur Dauer des Streams stoppt. Diese Methode implementiert die IMediaSeeking::GetStopPosition-Methode.
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: CPosPassThru.GetStopPosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9c6798d03e2935c991e12cded4d85a4972d54e7800d6aa79c70525b10276f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084070"
---
# <a name="cpospassthrugetstopposition-method"></a>CPosPassThru.GetStopPosition-Methode

Die -Methode ruft den Zeitpunkt ab, zu dem die `GetStopPosition` Wiedergabe relativ zur Dauer des Streams anzuhalten ist. Diese Methode implementiert die [**IMediaSeeking::GetStopPosition-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




