---
description: Ändert das dirty-Flag für den aktuellen Stream.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: CPersistStream.SetDirty-Methode (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909300"
---
# <a name="cpersiststreamsetdirty-method"></a>CPersistStream.SetDirty-Methode

Ändert das dirty-Flag für den aktuellen Stream.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fDirty* 
</dt> <dd>

Neues dirty-Flag für diesen Stream. **TRUE** bedeutet, dass die Daten nicht gespeichert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




