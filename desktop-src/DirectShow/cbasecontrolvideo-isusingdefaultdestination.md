---
description: Die IsUsingDefaultDestination-Methode bestimmt, ob der Renderer das Standardzielfenster verwendet.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: CBaseControlVideo.IsUsingDefaultDestination-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf254ec89cc6804af86c98abaaa0c53ae5f76a25766391529ca4de85bee7d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955219"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a>CBaseControlVideo.IsUsingDefaultDestination-Methode

Die `IsUsingDefaultDestination` -Methode bestimmt, ob der Renderer das Standardzielfenster verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn das Standardziel verwendet wird, andernfalls S \_ FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




