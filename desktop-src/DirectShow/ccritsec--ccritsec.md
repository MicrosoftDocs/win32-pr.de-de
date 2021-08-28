---
description: CCritSec.~CCritSec-Destruktor – Destruktormethode.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec.~CCritSec-Destruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d34665bb18a6ea9f6e76ad6332a5d7f344993067848c1b5e473893e702b62a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999610"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec.~CCritSec-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CCritSec();
```



## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**DeleteCriticalSection-Funktion auf,**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) um den kritischen Abschnitt zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

