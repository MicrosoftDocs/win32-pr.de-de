---
description: Mit der registermediatime-Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Crendererpospassthru. registermediatime-Methode (ctlutil. h)
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
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369659"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Crendererpospassthru. registermediatime-Methode (ctlutil. h)

Mit der **registermediatime** -Methode werden die Zeitstempel aus dem aktuellen Beispiel zwischengespeichert.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                  | Beschreibung                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                        |
| <dl> <dt>**VFW \_ E \_ Medien \_ Zeit \_ nicht \_ festgelegt**</dt> </dl> | Das Beispiel ist nicht mit einem Zeitstempel versehen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode speichert die Zeitstempel aus dem aktuellen Beispiel. Die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode ruft die gleichen Werte ab.

Der Filter sollte diese Methode für jedes empfangene Beispiel aufgerufen werden. Die-Methode ist überladen, um entweder einen Zeiger auf das Beispiel oder den Zeitstempelwert selbst zu akzeptieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




