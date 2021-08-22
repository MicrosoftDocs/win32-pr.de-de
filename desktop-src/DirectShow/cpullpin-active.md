---
description: Die Active-Methode erstellt einen Arbeitsthread, der Daten vom Ausgabepin abruft. Diese Methode committet auch die Zuweisung.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: CPullPin.Active-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073524"
---
# <a name="cpullpinactive-method"></a>CPullPin.Active-Methode

Die **Active-Methode** erstellt einen Arbeitsthread, der Daten vom Ausgabepin abruft. Diese Methode committet auch die Zuweisung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Die Pinverbindung wurde nicht ordnungsgemäß hergestellt.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Der Thread konnte nicht erstellt werden, oder der Thread ist bereits vorhanden.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, wenn der besitzende Filter aktiv wird. (Wenn Ihr Eingabepin von [**CBasePin**](cbasepin.md)abgeleitet wird, überschreiben Sie die [**CBasePin::Active-Methode.)**](cbasepin-active.md)

Rufen Sie vor dem Aufrufen dieser Methode die [**CPullPin::Verbinden-Methode**](cpullpin-connect.md) auf, um die Verbindung mit dem Ausgabepin herzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




