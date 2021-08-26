---
description: Die RegisterMediaTime-Methode speichert die Zeitstempel aus dem aktuellen Beispiel zwischen. Diese Methode verwendet die *Parameter StartTime* und *EndTime.*
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: CRendererPosPassThru.RegisterMediaTime-Methode (Ctlutil.h) – StartTime- und EndTime-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084110"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>CRendererPosPassThru.RegisterMediaTime-Methode (Ctlutil.h) – StartTime- und EndTime-Parameter

Die [**RegisterMediaTime-Methode**](crendererpospassthru-registermediatime.md) speichert die Zeitstempel aus dem aktuellen Beispiel zwischen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* 
</dt> <dd>

Beispielstartzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*EndTime* 
</dt> <dd>

Beispielendzeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode speichert die Zeitstempelwerte, die in *StartTime* und *EndTime* angegeben sind. Die [**CRendererPosPassThru::GetMediaTime-Methode**](crendererpospassthru-getmediatime.md) ruft die gleichen Werte ab.

Der Filter sollte diese Methode für jedes empfangene Beispiel aufrufen. Die -Methode wird überladen, um entweder einen Zeiger auf das Beispiel oder die Zeitstempelwerte selbst zu akzeptieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Ctlutil.h (include Streams.h)                                                                                   |
| Bibliothek | Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |



 

 




