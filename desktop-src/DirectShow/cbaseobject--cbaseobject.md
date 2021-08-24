---
description: 'CBaseObject.~CBaseObject-Destruktor : Destruktormethode.'
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: CBaseObject.~CBaseObject-Destruktor (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6508591f30a14e345cb67f9fe3a098dbaf357b6f60f57232af9f7af4570b6f6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640180"
---
# <a name="cbaseobjectcbaseobject-destructor"></a>CBaseObject.~CBaseObject-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CBaseObject();
```



## <a name="remarks"></a>Hinweise

Diese Methode dekrementt die Anzahl der Aktiv-Objekte. (Siehe [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseObject-Klasse**](cbaseobject.md)
</dt> </dl>

 

 




