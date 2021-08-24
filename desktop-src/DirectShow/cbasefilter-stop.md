---
description: Die Stop-Methode beendet den Filter. Diese Methode implementiert die IMediaFilter::Stop-Methode.
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: CBaseFilter.Stop-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 659ad34c01ca6c74a24f6bbf5f5bef42df46f94f06b7e03541f9caf3398b39e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768190"
---
# <a name="cbasefilterstop-method"></a>CBaseFilter.Stop-Methode

Die `Stop` -Methode beendet den Filter. Diese Methode implementiert die [**IMediaFilter::Stop-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBasePin::Inactive-Methode**](cbasepin-inactive.md) für jeden der verbundenen Pins des Filters auf. Außerdem wird der Status des Filters auf State \_ Stopped festgelegt.

Wenn der Filter beendet wird, sollte er Stichproben aus upstream ablehnen, die Übermittlung von Stichproben nachgeschaltet beenden, Arbeitsthreads herunterfahren und alle Ressourcen freigeben, die für das Streaming verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




