---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Ctransforminputpin. endflush-Methode (Transfrm. h)
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
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370737"
---
# <a name="ctransforminputpinendflush-method"></a>Ctransforminputpin. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang. Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Ausgabepin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**ctransformfilter:: endflush**](ctransformfilter-endflush.md) -Methode des Filters auf, um den Aufruf Downstream zu übermitteln. Anschließend wird die [**cbaseiniputpin:: endflush**](cbaseinputpin-endflush.md) -Methode der PIN aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




