---
description: Die RegisterMediaTime-Methode speichert die Zeitstempel aus dem aktuellen Beispiel zwischen.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: CRendererPosPassThru.RegisterMediaTime-Methode (Ctlutil.h)
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
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054380"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>CRendererPosPassThru.RegisterMediaTime-Methode (Ctlutil.h)

Die **RegisterMediaTime-Methode** speichert die Zeitstempel aus dem aktuellen Beispiel zwischen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                  | Beschreibung                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                        |
| <dl> <dt>**VFW \_ E \_ \_ MEDIENZEIT NICHT \_ \_ FESTGELEGT**</dt> </dl> | Das Beispiel ist nicht mit einem Zeitstempel versehen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode speichert die Zeitstempel aus dem aktuellen Beispiel. Die [**CRendererPosPassThru::GetMediaTime-Methode**](crendererpospassthru-getmediatime.md) ruft dieselben Werte ab.

Der Filter sollte diese Methode für jedes empfangene Beispiel aufrufen. Die -Methode wird überladen, um entweder einen Zeiger auf das Beispiel oder die Zeitstempelwerte selbst zu akzeptieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




