---
description: 'CBaseReferenceClock.CBaseReferenceClock-Konstruktor : Konstruktormethode.'
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: CBaseReferenceClock.CBaseReferenceClock-Konstruktor (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119938"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>CBaseReferenceClock.CBaseReferenceClock-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die IUnknown-Schnittstelle des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück. Legen Sie diesen Parameter nicht auf **NULL fest.**

</dd> <dt>

*pSched* 
</dt> <dd>

Zeiger auf ein [**WEBCAMSchedule-Objekt.**](camschedule.md) Bei **NULL** erstellt diese Methode ein **neuesCAMSchedule-Objekt.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




