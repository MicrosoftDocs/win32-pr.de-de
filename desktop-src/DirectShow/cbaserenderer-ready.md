---
description: Die Ready-Methode signalisiert, dass ein Zustandsübergang abgeschlossen ist.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: CBaseRenderer.Ready-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757520"
---
# <a name="cbaserendererready-method"></a>CBaseRenderer.Ready-Methode

Die `Ready` -Methode signalisiert, dass ein Zustandsübergang abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
void Ready();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode bewirkt, dass die [**CBaseRenderer::GetState-Methode**](cbaserenderer-getstate.md) S OK zurückgibt, was angibt, dass der Filter den Übergang in seinen \_ aktuellen Zustand abgeschlossen hat. Der Filter ruft diese Methode immer dann auf, wenn ein Zustandsübergang abgeschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 




