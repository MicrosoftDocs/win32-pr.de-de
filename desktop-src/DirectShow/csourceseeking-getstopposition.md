---
description: 'Die getstoppositionelle-Methode ruft die Zeit ab, zu der die Wiedergabe in Bezug auf die Dauer des Streams beendet wird. Diese Methode implementiert die imediaseeking:: getstoppositionelle-Methode.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Csourceseeking. getstoppositionelle-Methode (ctlutil. h)
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
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351381"
---
# <a name="csourceseekinggetstopposition-method"></a>Csourceseeking. getstoppositionelle-Methode

Die- `GetStopPosition` Methode ruft die Zeit ab, zu der die Wiedergabe in Bezug auf die Dauer des Streams beendet wird. Diese Methode implementiert die [**imediaseeking:: getstoppositionelle**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Endzeit wird von der Element Variablen [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




