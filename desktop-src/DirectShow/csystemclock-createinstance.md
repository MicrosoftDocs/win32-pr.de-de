---
description: Die Methode "kreateinstance" erstellt eine neue Instanz dieses Objekts.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Csystemclock. kreateinstance-Methode (sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365428"
---
# <a name="csystemclockcreateinstance-method"></a>Csystemclock. kreatzustance-Methode

Die- `CreateInstance` Methode erstellt eine neue Instanz dieses Objekts.

## <a name="syntax"></a>Syntax


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine neue Instanz dieses-Objekts zurück.

## <a name="remarks"></a>Bemerkungen

Die Klassenfactory ruft diese Methode auf, um das Objekt zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sysclock. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




