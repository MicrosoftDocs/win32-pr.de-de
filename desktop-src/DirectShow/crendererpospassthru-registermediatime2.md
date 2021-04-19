---
description: Mit der registermediatime-Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert. Diese Methode verwendet die Parameter " *StartTime* " und " *EndTime* ".
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: 'Crendererpospassthru. registermediatime-Methode (ctlutil. h): StartTime-und EndTime-Parameter'
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
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372551"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Crendererpospassthru. registermediatime-Methode (ctlutil. h): StartTime-und EndTime-Parameter

Mit der [**registermediatime**](crendererpospassthru-registermediatime.md) -Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.

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

Beispiel Startzeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*EndTime* 
</dt> <dd>

Beispiel Endzeit in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode speichert die Zeitstempel Werte, die in " *StartTime* " und " *EndTime*" angegeben sind. Die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode ruft die gleichen Werte ab.

Der Filter sollte diese Methode für jedes empfangene Beispiel aufgerufen werden. Die-Methode ist überladen, um entweder einen Zeiger auf das Beispiel oder den Zeitstempelwert selbst zu akzeptieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Ctlutil. h (Include Streams. h)                                                                                   |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |



 

 




