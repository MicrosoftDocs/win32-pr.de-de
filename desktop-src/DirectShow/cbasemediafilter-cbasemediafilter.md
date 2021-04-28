---
description: 'CBaseMediaFilter.CBaseMediaFilter-Konstruktor : Konstruktormethode.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: CBaseMediaFilter.CBaseMediaFilter-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096318"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>CBaseMediaFilter.CBaseMediaFilter-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.

</dd> <dt>

*Clsid* 
</dt> <dd>

Klassenbezeichner des Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein anderes Objekt das Objekt enthält oder aggregiert, kann `CBaseMediaFilter` die **CCritSec-Sperre** für das Objekt extern `CBaseMediaFilter` sein. Übergeben Sie in diesem Fall einen Zeiger auf die Sperre in *pLock*.

Andernfalls können Sie:

-   Leiten Sie eine Klasse ab, die sowohl als auch `CBaseMediaFilter` **CCritSec erbt.** Übergeben *Sie für pLock* den this-Zeiger.
-   Leiten Sie eine Klasse ab, die eine `CBaseMediaFilter` **CCritSec-Membervariable erbt und** enthält. Übergeben Sie für *pLock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




