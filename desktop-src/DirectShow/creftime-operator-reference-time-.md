---
description: Der Reference \_ time ()-Operator wandelt das Objekt in einen Verweis \_ Zeit Datentyp um.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: REFERENCE_TIME-Methode ("Ref time. h")
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
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372433"
---
# <a name="creftimeoperator-reference_time-method"></a>Methode zum Aufrufen der Methode "forf time. Operator" \_

Der- `REFERENCE_TIME()` Operator wandelt das Objekt in einen [**Verweis \_ Zeit**](reference-time.md) Datentyp um.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von " [**krefitime:: m \_ time**](creftime-m-time.md)" zurück.

## <a name="remarks"></a>Bemerkungen

Im folgenden Beispiel wird gezeigt, wie Sie diesen Umwandlungs Operator verwenden:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref time. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




