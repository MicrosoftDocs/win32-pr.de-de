---
description: Die notifymediatype-Methode informiert das-Objekt über den aktuellen Medientyp.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Cimagezuzuordcator. notifymediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372661"
---
# <a name="cimageallocatornotifymediatype-method"></a>Cimagezuzuordcator. notifymediatype-Methode

Die- `NotifyMediaType` Methode informiert das-Objekt über den aktuellen Medientyp.

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

Der besitzende Filter sollte diese Methode immer dann aufzurufen, wenn sich der Medientyp ändert. Dies tritt normalerweise auf, wenn die PIN zum ersten Mal eine Verbindung herstellt und nach einer Änderung des dynamischen Formats. Der Zuweiser verwendet den Medientyp zum Überprüfen der vorgeschlagenen zuordnereigenschaften und auch beim Erstellen von Medien Beispielen.

Das **cimagezuordcator** -Objekt speichert den *pmediatype* -Zeiger in der Member-Variablen " **m \_ pmediatype** ". Wenn der Aufrufer das **cmediatype** -Objekt freigeben muss, sollte es daher die Zuweisung aktualisieren, indem diese Methode erneut aufgerufen wird, entweder mit einem neuen Zeiger oder mit einem **null** -Wert. Andernfalls kann ein Fehler auftreten, wenn die Zuweisung versucht, auf den alten Zeiger zu verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagezuordcator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




