---
description: Die OnWaitEnd-Methode wird aufgerufen, wenn eine Wartezeit endet.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: CBaseVideoRenderer.OnWaitEnd-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b130bf38833951cad4f82fd559c0299d2aea86854ca0ab5545f3f2794ab9b4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432470"
---
# <a name="cbasevideorendereronwaitend-method"></a>CBaseVideoRenderer.OnWaitEnd-Methode

Die OnWaitEnd-Methode wird aufgerufen, wenn eine Wartezeit endet.

## <a name="syntax"></a>Syntax


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion führt nur die Leistungsprotokollierung durch. Sie wird aufgerufen, wenn der Thread vom Warten im Fenster aufgeweckt wird oder wenn das nächste Beispiel gerendert werden soll. Sie kann schließlich verwendet werden, um Informationen zu sammeln, die die Synchronisierung steuern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




