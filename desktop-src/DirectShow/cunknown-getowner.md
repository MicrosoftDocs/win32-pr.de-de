---
description: Die GetOwner-Methode ruft einen Zeiger auf die IUnknown-Schnittstelle der besitzenden Komponente ab. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls besitzt sich die Komponente selbst.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: CUnknown.GetOwner-Methode (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076040"
---
# <a name="cunknowngetowner-method"></a>CUnknown.GetOwner-Methode

Die `GetOwner` -Methode ruft einen Zeiger auf die **IUnknown-Schnittstelle** der besitzenden Komponente ab. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls besitzt sich die Komponente selbst.

## <a name="syntax"></a>Syntax


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die steuernde **IUnknown-Schnittstelle** zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




