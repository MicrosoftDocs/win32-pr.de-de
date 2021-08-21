---
description: Die Active-Methode wird aufgerufen, wenn der Zustand in "Angehalten" oder "Wird ausgeführt" umgeschaltet wird.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: CBaseRenderer.Active-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df5ec659b5e76940ebf279e3feb8995d34380db0543d9eebcf42c1f3bff8c0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954969"
---
# <a name="cbaserendereractive-method"></a>CBaseRenderer.Active-Methode

Die `Active` -Methode wird aufgerufen, wenn der Zustand in "Angehalten" oder "Wird ausgeführt" umgeschaltet wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der Eingabepin ruft diese Methode aus seiner eigenen [**CRendererInputPin::Active-Methode**](crendererinputpin-active.md) auf. Diese Methode führt in der Basisklasse nichts aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




