---
description: 'CSystemClock.CSystemClock-Konstruktor : Konstruktormethode.'
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: CSystemClock.CSystemClock-Konstruktor (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095198"
---
# <a name="csystemclockcsystemclock-constructor"></a>CSystemClock.CSystemClock-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf den **HRESULT-Wert.** Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sysclock.h (einschließlich Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




