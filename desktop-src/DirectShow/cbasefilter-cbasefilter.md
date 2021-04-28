---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) -Konstruktormethode.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT*) -Konstruktor (Amfilter.h)
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
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120108"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) -Konstruktor

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

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

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

## <a name="remarks"></a>Bemerkungen

Für das kritische Abschnittsobjekt würden Sie in der Regel einen der folgenden Schritte ausführen:

-   Leiten Sie eine Klasse ab, die sowohl **CBaseFilter** als auch **CCritSec** erbt. Übergeben Sie für *pLock* den `this` Zeiger.
-   Leiten Sie eine Klasse ab, die **CBaseFilter erbt** und eine **CCritSec-Membervariable** enthält. Übergeben *Sie für pLock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




