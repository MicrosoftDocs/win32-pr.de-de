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
ms.openlocfilehash: 264363ebb7194504dd16a94c0835bab0a4fe0163edd31329b77853510c9523db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917010"
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

Klassenbezeichner des -Objekts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein anderes Objekt das Objekt enthält oder aggregiert, kann `CBaseMediaFilter` die **CCritSec-Sperre** für das Objekt extern `CBaseMediaFilter` sein. Übergeben Sie in diesem Fall einen Zeiger auf die Sperre in *pLock*.

Andernfalls können Sie:

-   Leiten Sie eine Klasse ab, die sowohl als auch `CBaseMediaFilter` **CCritSec erbt.** Übergeben *Sie für pLock* den this-Zeiger.
-   Leiten Sie eine Klasse ab, die eine `CBaseMediaFilter` **CCritSec-Membervariable erbt und** enthält. Übergeben *Sie für pLock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




