---
description: Die NotifyMediaType-Methode benachrichtigt das CDrawImage-Objekt über den aktuellen Medientyp.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: CDrawImage.NotifyMediaType-Methode (Winutil.h)
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
ms.openlocfilehash: 3df1f904bb5c2acfc328e8779da6135f901de9601cea6735de21b2e76aeea9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656791"
---
# <a name="cdrawimagenotifymediatype-method"></a>CDrawImage.NotifyMediaType-Methode

Die `NotifyMediaType` -Methode benachrichtigt das **CDrawImage-Objekt** über den aktuellen Medientyp.

## <a name="syntax"></a>Syntax


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt**](cmediatype.md) oder **NULL,** um den Medientyp zu löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der besitzende Filter sollte diese Methode immer dann aufrufen, wenn sich der Medientyp ändert. In der Regel tritt dies auf, wenn die Stecknadel zum ersten Mal eine Verbindung herstellt, und nach einer dynamischen Formatänderung.

Das **CDrawImage-Objekt** speichert den *pMediaType-Zeiger* in der m **\_ pMediaType-Membervariablen.** Wenn der Aufrufer daher das **CMediaType-Objekt** freigeben muss, sollte er das **CDrawImage-Objekt** aktualisieren, indem er diese Methode erneut aufruft, entweder mit einem neuen Zeiger oder mit einem **NULL-Wert.** Andernfalls kann ein Fehler auftreten, wenn das **CDrawImage-Objekt** versucht, auf den alten Zeiger zu verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




