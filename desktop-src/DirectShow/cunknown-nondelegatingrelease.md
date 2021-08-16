---
description: Dekrementt den Verweiszähler für das -Objekt. Diese Methode implementiert die INonDelegatingUnknown::NonDelegatingRelease-Methode.
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: CUnknown.NonDelegatingRelease-Methode (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ac5145e1776602c5bb358805c45ec271766fe918b7924d948e286ae32b31794
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821954"
---
# <a name="cunknownnondelegatingrelease-method"></a>CUnknown.NonDelegatingRelease-Methode

Dekrementt den Verweiszähler für das -Objekt. Diese Methode implementiert die **INonDelegatingUnknown::NonDelegatingRelease-Methode.**

## <a name="syntax"></a>Syntax


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Verweiszähler zurück.

## <a name="remarks"></a>Hinweise

Wenn der Verweiszähler 0 (null) erreicht, löscht sich das Objekt selbst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




