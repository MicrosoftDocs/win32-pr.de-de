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
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119798"
---
# <a name="ccritsecccritsec-constructor"></a>CCritSec.CCritSec-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CCritSec();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor verfügt über keine Parameter.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**InitializeCriticalSection-Funktion auf,**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) um den kritischen Abschnitt zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (streams.h enthalten)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

