---
description: Konstruktormethode.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Ccritsec. ccritsec-Konstruktor (wxutil. h)
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
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374032"
---
# <a name="ccritsecccritsec-constructor"></a>Ccritsec. ccritsec-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CCritSec();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) -Funktion auf, um den kritischen Abschnitt zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> </dl>

 

