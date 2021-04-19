---
description: Dekonstruktormethode.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Ccritsec. ~ ccritsec-debugtor (wxutil. h)
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
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371671"
---
# <a name="ccritsecccritsec-destructor"></a>Ccritsec. ~ ccritsec-Dekonstruktor

Dekonstruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CCritSec();
```



## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) -Funktion auf, um den kritischen Abschnitt zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> </dl>

 

