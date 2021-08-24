---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) konstruktor – Konstruktormethode.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: CBaseFilter.CBaseFilter(const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT*) konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 023de6fd8df37930954b59114e4e00fa409b7803a83ae15b31f6816c4dfdffbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640710"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Filters enthält, zu Debugzwecken.

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

Klassenbezeichner (CLSID) des Filters.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Der Konstruktor ignoriert diesen Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Für das kritische Abschnittsobjekt führen Sie in der Regel einen der folgenden Schritte aus:

-   Leiten Sie eine Klasse ab, die **sowohl CBaseFilter** als auch **CCritSec erbt.** Übergeben *Sie für pLock* den `this` Zeiger.
-   Leiten Sie eine Klasse ab, die **CBaseFilter erbt** und eine **CCritSec-Membervariable** enthält. Übergeben *Sie für pLock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




