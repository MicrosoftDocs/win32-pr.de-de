---
description: Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: CPersistStream.IsDirty-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108440"
---
# <a name="cpersiststreamisdirty-method"></a>CPersistStream.IsDirty-Methode

Gibt an, ob sich das Objekt seit dem letzten Speichern im aktuellen Stream geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Filter speichern muss, und S \_ FALSE, wenn er nicht speichern muss.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die **IPersistStream::IsDirty-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




