---
description: Die CompleteStateChange-Methode bestimmt, ob ein Übergang in den angehaltenen Zustand abgeschlossen ist.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: CBaseRenderer.CompleteStateChange-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872360"
---
# <a name="cbaserenderercompletestatechange-method"></a>CBaseRenderer.CompleteStateChange-Methode

Die `CompleteStateChange` -Methode bestimmt, ob ein Übergang in den angehaltenen Zustand abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldState* 
</dt> <dd>

Zustand vor dem Übergang.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Übergang abgeschlossen ist. Andernfalls wird S \_ FALSE zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::P ause-Methode**](cbaserenderer-pause.md) ruft diese Methode auf, um den Status des Zustandsübergangs zu aktualisieren. Im Allgemeinen wird der Übergang zu angehalten erst abgeschlossen, wenn der Filter ein Beispiel empfängt. In einigen Situationen wird der Übergang jedoch sofort abgeschlossen, z. B. wenn der Filter nicht verbunden ist oder wenn das Ende des Streams erreicht wurde. Diese Methode überprüft die verschiedenen Kriterien und ruft dann die [**CBaseRenderer::Ready-Methode**](cbaserenderer-ready.md) oder die [**CBaseRenderer::NotReady-Methode**](cbaserenderer-notready.md) auf, um den Übergangsstatus zu aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




