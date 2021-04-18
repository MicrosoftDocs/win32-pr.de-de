---
description: Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Camthread:: m_AccessLock Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365548"
---
# <a name="camthreadm_accesslock-member"></a>Camthread:: m \_ accesslock-Member

Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Bemerkungen

Die Methoden " [**camthread:: Create**](camthread-create.md) " und " [**camthread:: callworker**](camthread-callworker.md) " enthalten diese Sperre, um Vorgänge für den Thread zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




