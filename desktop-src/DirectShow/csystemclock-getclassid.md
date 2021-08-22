---
description: Die GetClassID-Methode ruft den Klassenbezeichner (CLSID) des Objekts ab. Diese Methode implementiert die IPersist::GetClassID-Methode.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: CSystemClock.GetClassID-Methode (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2afb141c3a79255504eb13dadb39cc0fb5094c19e0979db04c251f1e2fe75133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317190"
---
# <a name="csystemclockgetclassid-method"></a>CSystemClock.GetClassID-Methode

Die `GetClassID` -Methode ruft den Klassenbezeichner (CLSID) des -Objekts ab. Diese Methode implementiert die **IPersist::GetClassID-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pClsID* 
</dt> <dd>

Zeiger auf eine Variable, die den Wert CLSID \_ SystemClock empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock-Klasse<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Sysclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




