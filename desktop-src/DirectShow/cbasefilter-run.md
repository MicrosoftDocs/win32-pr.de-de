---
description: 'Die Run-Methode führt den Filter aus. Diese Methode implementiert die imediafilter:: Run-Methode.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Cbasefilter. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351279"
---
# <a name="cbasefilterrun-method"></a>Cbasefilter. Run-Methode

Die- `Run` Methode führt den Filter aus. Diese Methode implementiert die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tSTART* 
</dt> <dd>

Verweis Zeit entsprechend der streamzeit 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter angehalten wurde, hält diese Methode den Filter an, indem er die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode aufrufen. Anschließend wird die [**cbasepin:: Run**](cbasepin-run.md) -Methode für jeden verbundenen Pins des Filters aufgerufen. Schließlich wird die [**cbasefilter:: m \_ State**](cbasefilter-m-state.md) Member-Variable auf State Running festgelegt \_ .

Die streamzeit wird als aktuelle Verweis Zeit abzüglich *tSTART* berechnet. Ein Medien Beispiel mit einem Zeitstempel von NULL sollte zum Zeitpunkt *tSTART* gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




