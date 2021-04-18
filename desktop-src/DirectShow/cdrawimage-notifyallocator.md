---
description: Die notifyzucator-Methode informiert das cdrawimage-Objekt darüber, ob die Zuweisung für die Verbindung ein cimagezuordcator-Objekt ist.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Cdrawimage. notifyzucator-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352083"
---
# <a name="cdrawimagenotifyallocator-method"></a>Cdrawimage. notifyzucator-Methode

Die- `NotifyAllocator` Methode informiert das **cdrawimage** -Objekt darüber, ob die Zuweisung für die Verbindung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.

## <a name="syntax"></a>Syntax


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*busingimagezuordcator* 
</dt> <dd>

Boolescher Wert, der angibt, welche Art von Zuweisungstyp verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der besitzende Filter sollte diese Methode anrufen, nachdem die Pins einem Zuweiser zugestimmt haben. Wenn der Filter weiß, dass es sich bei der Zuweisung um ein **cimagezuordnerobjekt** handelt, sollte diese Methode mit dem Wert " **true**" aufgerufen werden. (In der Regel kennt der Filter dies nur, wenn er die betreffende Zuweisung besitzt.) Andernfalls sollte diese Methode mit dem Wert **false** aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




