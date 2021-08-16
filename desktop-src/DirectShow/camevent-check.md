---
description: Die Check-Methode überprüft, ob das Ereignis ohne Blockierung festgelegt ist.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: WEBCAMEvent.Check-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a961d7df45ddac7ade5e39f91c1aed56609ce2d2eeb8e7423799c9a4903884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955539"
---
# <a name="cameventcheck-method"></a>CAMEvent.Check-Methode

Die `Check` -Methode überprüft, ob das Ereignis ohne Blockierung festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
BOOL Check();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

Gibt **TRUE zurück,** wenn das Ereignis festgelegt ist, andernfalls **FALSE.** Diese Methode ruft die [**METHODE WEBCAMEvent::Wait**](camevent-wait.md) mit einem Time out von 0 (null) auf. Wenn es sich bei dem Objekt um ein Ereignis zur automatischen Zurücksetzung handelt, setzt diese Methode das Ereignis zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMEvent-Klasse**](camevent.md)
</dt> </dl>

 

 




