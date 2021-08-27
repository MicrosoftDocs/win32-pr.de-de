---
description: Der REFERENCE \_ TIME()-Operator casts the object to a REFERENCE \_ TIME data type.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: CRefTime.operator REFERENCE_TIME-Methode (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a084d4e142f57b724343ac5a353461b41aac0be216b8e3851bc8b7e40000a1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108030"
---
# <a name="creftimeoperator-reference_time-method"></a>CRefTime.operator REFERENCE \_ TIME-Methode

Der `REFERENCE_TIME()` -Operator gibt das -Objekt in einen [**REFERENCE \_ TIME-Datentyp**](reference-time.md) um.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CRefTime::m \_ time zurück.**](creftime-m-time.md)

## <a name="remarks"></a>Hinweise

Im folgenden Beispiel wird die Verwendung dieses Cast-Operators veranschaulicht:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Reftime.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




