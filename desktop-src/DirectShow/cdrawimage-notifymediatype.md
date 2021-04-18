---
description: Die notifymediatype-Methode benachrichtigt das cdrawimage-Objekt des aktuellen Medientyps.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Cdrawimage. notifymediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365761"
---
# <a name="cdrawimagenotifymediatype-method"></a>Cdrawimage. notifymediatype-Methode

Die- `NotifyMediaType` Methode benachrichtigt das **cdrawimage** -Objekt des aktuellen Medientyps.

## <a name="syntax"></a>Syntax


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediatype* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt oder **null** , um den Medientyp zu löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der besitzende Filter sollte diese Methode immer dann aufzurufen, wenn sich der Medientyp ändert. Dies tritt normalerweise auf, wenn die PIN zum ersten Mal eine Verbindung herstellt und nach einer Änderung des dynamischen Formats.

Das **cdrawimage** -Objekt speichert den *pmediatype* -Zeiger in der Member-Variablen " **m \_ pmediatype** ". Wenn der Aufrufer also das **cmediatype** -Objekt freigeben muss, sollte es das **cdrawimage** -Objekt durch erneutes Aufrufen dieser Methode aktualisieren, entweder mit einem neuen Zeiger oder mit einem **null** -Wert. Andernfalls kann ein Fehler auftreten, wenn das **cdrawimage** -Objekt versucht, auf den alten Zeiger zu verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




