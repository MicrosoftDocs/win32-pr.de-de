---
description: 'Die getstoppositionelle-Methode ruft die Zeit ab, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die imediaseeking:: getstoppositionelle-Methode.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Cpospassthru. getstoppositionelle-Methode (ctlutil. h)
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
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364534"
---
# <a name="cpospassthrugetstopposition-method"></a>Cpospassthru. getstoppositionelle-Methode

Die- `GetStopPosition` Methode ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die [**imediaseeking:: getstoppositionelle**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) -Methode.

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

 

 




