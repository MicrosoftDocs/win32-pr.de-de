---
description: Die setabortsignal-Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Cbaserderderer. * tabortsignal-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369123"
---
# <a name="cbaserenderersetabortsignal-method"></a>Cbaserderderer. * tabortsignal-Methode

Die- `SetAbortSignal` Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.

## <a name="syntax"></a>Syntax


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*babort* 
</dt> <dd>

Boolescher Wert, der angibt, ob das Rendering beendet werden soll. Wenn der Wert **true** ist, werden keine weiteren Beispiele für den Filter angezeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt das Flag [**cbaserdenderer:: m \_ babort**](cbaserenderer-m-babort.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




