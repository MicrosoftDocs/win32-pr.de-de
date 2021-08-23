---
description: Die GetStopPosition-Methode ruft die Zeit ab, zu der die Wiedergabe beendet wird, relativ zur Dauer des Streams. Diese Methode implementiert die IMediaSeeking::GetStopPosition-Methode.
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: CSourceSeeking.GetStopPosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073324"
---
# <a name="csourceseekinggetstopposition-method"></a>CSourceSeeking.GetStopPosition-Methode

Die `GetStopPosition` -Methode ruft die Zeit ab, zu der die Wiedergabe beendet wird, relativ zur Dauer des Streams. Diese Methode implementiert die [**IMediaSeeking::GetStopPosition-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition)

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

Zeiger auf eine Variable, die die Beendigungszeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

## <a name="remarks"></a>Hinweise

Die Beendigungszeit wird von der [**CSourceSeeking::m \_ rtStop-Membervariablen**](csourceseeking-m-rtstop.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




