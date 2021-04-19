---
description: Die sendquality-Methode sendet eine Qualitäts Meldung, um anzugeben, was der Lieferant mit der Qualität tun soll.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Cbasevideorenderer. sendquality-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369418"
---
# <a name="cbasevideorenderersendquality-method"></a>Cbasevideorenderer. sendquality-Methode

Die- `SendQuality` Methode sendet eine Qualitäts Meldung, um anzugeben, was der Lieferant mit der Qualität tun soll.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*trlate* 
</dt> <dd>

Die Zeitspanne, nach der der Rahmen spät ist.

</dd> <dt>

*trrealstream* 
</dt> <dd>

Currentstream-Zeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion sendet eine Qualitäts Steuerungs Nachricht zum Steuern der Qualitäts Verwaltung. Die Art der Qualitäts Meldung (d. h., ob die Anzahl der Stichproben reduziert oder erhöht werden soll) wird in der Quality Management-Implementierung in dieser abgeleiteten Klasse festgelegt (siehe [**cbasevideorenderer:: schulddrawsamplenow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




