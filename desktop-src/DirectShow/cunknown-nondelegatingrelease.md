---
description: 'Dekremente den Verweis Zähler für das Objekt. Diese Methode implementiert die inondelegatingunknown:: nondelegatingrelease-Methode.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Cunknown. nondelegatingrelease-Methode (ComBase. h)
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
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372667"
---
# <a name="cunknownnondelegatingrelease-method"></a>Cunknown. nondelegatingrelease-Methode

Dekremente den Verweis Zähler für das Objekt. Diese Methode implementiert die **inondelegatingunknown:: nondelegatingrelease** -Methode.

## <a name="syntax"></a>Syntax


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Verweis Zähler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Verweis Zähler Null erreicht, löscht das Objekt sich selbst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




