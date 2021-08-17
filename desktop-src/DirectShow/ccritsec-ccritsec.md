---
description: 'CCritSec.CCritSec-Konstruktor : Konstruktormethode.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: CCritSec.CCritSec-Konstruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fce4cb5edb9765e7f69726188e5ed0ba2017df7d6fa90cae0bfa059b89fc939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688990"
---
# <a name="ccritsecccritsec-constructor"></a>CCritSec.CCritSec-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CCritSec();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**InitializeCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) auf, um den kritischen Abschnitt zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

