---
description: 'CCritSec.~CCritSec-Destruktor : Destruktormethode.'
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
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095808"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec.~CCritSec-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CCritSec();
```



## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**DeleteCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) auf, um den kritischen Abschnitt zu löschen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

