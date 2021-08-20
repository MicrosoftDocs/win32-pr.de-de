---
description: Die GetRequest-Methode wartet auf die nächste Threadanforderung.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: CSourceStream.GetRequest-Methode (Source.h)
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
ms.openlocfilehash: e28a8e57535a49903cd2a7b23fb0d0d179bf910b20225042c65b3bdcda620f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073204"
---
# <a name="csourcestreamgetrequest-method"></a>CSourceStream.GetRequest-Methode

Die `GetRequest` -Methode wartet auf die nächste Threadanforderung.

## <a name="syntax"></a>Syntax


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die nächste Threadanforderung zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**METHODECAMThread::GetRequest.**](camthread-getrequest.md) Der Rückgabewert wird in den folgenden aufzählten Typ umgeändert:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




