---
description: Stellt die Initialisierung für einen Thread zur Seite.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: CMsgThread.OnThreadInit-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9105bf8399b036421c5360c62a63d8c3fac44471adc13b9e8c224fb0eb84e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831840"
---
# <a name="cmsgthreadonthreadinit-method"></a>CMsgThread.OnThreadInit-Methode

Stellt die Initialisierung für einen Thread zur Seite.

## <a name="syntax"></a>Syntax


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Überschreiben Sie diese Funktion, wenn Sie ihre eigene spezifische Initialisierung beim Starten des Threads verwenden möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




