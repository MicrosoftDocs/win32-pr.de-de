---
description: Die Check-Methode überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Camevent. Check-Methode (wxutil. h)
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
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367437"
---
# <a name="cameventcheck-method"></a>Camevent. Check-Methode

Die- `Check` Methode überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.

## <a name="syntax"></a>Syntax


```C++
BOOL Check();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Gibt " **true** " zurück, wenn das Ereignis festgelegt ist, andernfalls " **false** ". Diese Methode ruft die Methode " [**camevent:: Wait**](camevent-wait.md) " mit einem Timeout von 0 (null) auf. Wenn das Objekt ein automatisches Zurücksetzungs Ereignis ist, setzt diese Methode das Ereignis zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camevent-Klasse**](camevent.md)
</dt> </dl>

 

 




