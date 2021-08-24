---
description: Die Inactive-Methode wird aufgerufen, wenn der Zustand in Beendet wechselt.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: CBaseRenderer.Inactive-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652400"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer.Inactive-Methode

Die `Inactive` -Methode wird aufgerufen, wenn der Zustand in Beendet wechselt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der Eingabepin ruft diese Methode aus seiner eigenen [**CRendererInputPin::Inactive-Methode**](crendererinputpin-inactive.md) auf. Der Filter ruft die [**CBaseRenderer::ClearPendingSample-Methode**](cbaserenderer-clearpendingsample.md) auf, um das neueste Beispiel frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




