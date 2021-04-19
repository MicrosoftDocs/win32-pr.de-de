---
description: Die GetOwner-Methode ruft einen Zeiger auf die IUnknown-Schnittstelle der besitzenden Komponente ab. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls ist die Komponente eigenständig.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Cunknown. GetOwner-Methode (ComBase. h)
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
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370271"
---
# <a name="cunknowngetowner-method"></a>Cunknown. GetOwner-Methode

Die- `GetOwner` Methode ruft einen Zeiger auf die **IUnknown** -Schnittstelle der besitzenden Komponente ab. Bei einer aggregierten Komponente ist der Besitzer die äußere Komponente. Andernfalls ist die Komponente eigenständig.

## <a name="syntax"></a>Syntax


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die steuernde **IUnknown** -Schnittstelle zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




