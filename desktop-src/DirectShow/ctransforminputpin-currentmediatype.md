---
description: 'CTransformInputPin.CurrentMediaType-Methode: Die CurrentMediaType-Methode ruft den Medientyp für die aktuelle Pinverbindung ab.'
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: CTransformInputPin.CurrentMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 011f4eeda7f4a278baeceeadc7c21a822ae02b74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084988"
---
# <a name="ctransforminputpincurrentmediatype-method"></a>CTransformInputPin.CurrentMediaType-Methode

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



 

 




