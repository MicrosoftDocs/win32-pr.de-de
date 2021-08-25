---
description: 'CTransformInputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: CTransformInputPin.BreakConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad97061bda8ec4703464d21ad4817cfd97740f4a98904255150ce75fba37c425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812890"
---
# <a name="ctransforminputpinbreakconnect-method"></a>CTransformInputPin.BreakConnect-Methode

Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseInputPin::BreakConnect-Methode.**](cbaseinputpin-breakconnect.md) Sie ruft die [**CTransformFilter::BreakConnect-Methode**](ctransformfilter-breakconnect.md) des Filters auf, die \_ S OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::BreakConnect-Methode** überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




