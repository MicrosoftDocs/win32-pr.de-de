---
description: Die aktive Methode erstellt einen Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Diese Methode führt auch einen Commit für die Zuweisung aus.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Cpullpin. Active-Methode (pullpin. h)
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
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354842"
---
# <a name="cpullpinactive-method"></a>Cpullpin. Active-Methode

Die **aktive** Methode erstellt einen Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Diese Methode führt auch einen Commit für die Zuweisung aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                                   |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Die PIN-Verbindung wurde nicht ordnungsgemäß eingerichtet.<br/>          |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Der Thread konnte nicht erstellt werden, oder der Thread ist bereits vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, wenn der besitzende Filter aktiv wird. (Wenn Ihre Eingabe-PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie die [**cbasepin:: Active**](cbasepin-active.md) -Methode.)

Rufen Sie vor dem Aufrufen dieser Methode die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode auf, um die Verbindung mit der Ausgabepin herzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




