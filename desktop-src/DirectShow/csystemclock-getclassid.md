---
description: 'Die GetClassID-Methode ruft den Klassen Bezeichner (CLSID) des-Objekts ab. Diese Methode implementiert die ipersistent:: GetClassID-Methode.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Csystemclock. GetClassID-Methode (sysclock. h)
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
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365845"
---
# <a name="csystemclockgetclassid-method"></a>Csystemclock. GetClassID-Methode

Die- `GetClassID` Methode ruft den Klassen Bezeichner (CLSID) des-Objekts ab. Diese Methode implementiert die **ipersistent:: GetClassID-** Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclsid* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert CLSID \_ systemclock empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Csystemclock-Klasse<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Sysclock. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




