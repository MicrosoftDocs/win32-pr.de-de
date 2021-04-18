---
description: Die getrequestparam-Methode ruft die aktuelle Anforderung ab.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Camthread. getrequestparam-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371239"
---
# <a name="camthreadgetrequestparam-method"></a>Camthread. getrequestparam-Methode

Die- `GetRequestParam` Methode ruft die aktuelle Anforderung ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des-Parameters zurück, der zuletzt an die Methode " [**camthread:: callworker**](camthread-callworker.md) " übergeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




