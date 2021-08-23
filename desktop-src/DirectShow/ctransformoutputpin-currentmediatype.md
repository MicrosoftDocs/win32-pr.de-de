---
description: 'CTransformOutputPin.CurrentMediaType-Methode: Die CurrentMediaType-Methode ruft den Medientyp für die aktuelle Pinverbindung ab.'
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: CTransformOutputPin.CurrentMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b223c8c75cd2345c80b5f0905ef7c6699ccc2499b209cbd17681bec5fec01142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756770"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>CTransformOutputPin.CurrentMediaType-Methode

Die `CurrentMediaType` -Methode ruft den Medientyp für die aktuelle Pinverbindung ab.

## <a name="syntax"></a>Syntax


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf die [**CBasePin::m \_ mt-Membervariable**](cbasepin-m-mt.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




