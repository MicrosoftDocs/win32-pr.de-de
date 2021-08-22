---
description: Die OnWaitStart-Methode aktualisiert die Wartezeiten, die nicht gewartet wurden.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: CBaseVideoRenderer.OnWaitStart-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bc3b895f27490377fd5de188b7cea8ccd429c55d36a5cdd0fea4ce025bac29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502600"
---
# <a name="cbasevideorendereronwaitstart-method"></a>CBaseVideoRenderer.OnWaitStart-Methode

Die `OnWaitStart` -Methode aktualisiert die Wartezeiten und wartet nicht.

## <a name="syntax"></a>Syntax


```C++
void OnWaitStart();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion wird aufgerufen, wenn mit dem Warten auf ein Renderingereignis beginnt. Es wird nur für Leistungsmessungen verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




