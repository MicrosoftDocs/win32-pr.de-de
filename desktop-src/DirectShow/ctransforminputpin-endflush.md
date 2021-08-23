---
description: 'CTransformInputPin.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang. Diese Methode implementiert die IPin::EndFlush-Methode.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: CTransformInputPin.EndFlush-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bca2231f36c3d37f58bb740ddf55132d1c63babba6054629b2a76cc5d7866646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687220"
---
# <a name="ctransforminputpinendflush-method"></a>CTransformInputPin.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang. Diese Methode implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Ausgabepin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CTransformFilter::EndFlush-Methode**](ctransformfilter-endflush.md) des Filters auf, um den Aufruf nachgeschaltet zu liefern. Anschließend wird die [**CBaseInputPin::EndFlush-Methode**](cbaseinputpin-endflush.md) des Pins aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




