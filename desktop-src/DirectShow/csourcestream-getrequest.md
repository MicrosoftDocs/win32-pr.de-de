---
description: Die GetRequest-Methode wartet auf die nächste Thread Anforderung.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Csourcestream. GetRequest-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366774"
---
# <a name="csourcestreamgetrequest-method"></a>Csourcestream. GetRequest-Methode

Die- `GetRequest` Methode wartet auf die nächste Thread Anforderung.

## <a name="syntax"></a>Syntax


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die nächste Thread Anforderung zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die Methode " [**camthread:: GetRequest**](camthread-getrequest.md) ". Der Rückgabewert wird in den folgenden enumerierten Typ umgewandelt:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




