---
description: Die CreateInstance-Methode erstellt eine neue Instanz dieses Objekts.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: CSystemClock.CreateInstance-Methode (Sysclock.h)
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
ms.openlocfilehash: 63626804ad4d067e5067170e0fc17cc83c179a906c0e625bb02a3ffb8a4ef197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687330"
---
# <a name="csystemclockcreateinstance-method"></a>CSystemClock.CreateInstance-Methode

Die `CreateInstance` -Methode erstellt eine neue Instanz dieses -Objekts.

## <a name="syntax"></a>Syntax


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die aggregierende **IUnknown-Schnittstelle.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine neue Instanz dieses -Objekts zurück.

## <a name="remarks"></a>Hinweise

Die Klassenfactory ruft diese Methode auf, um das -Objekt zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sysclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




