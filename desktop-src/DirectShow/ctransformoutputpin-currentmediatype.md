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
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094908"
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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




