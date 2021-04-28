---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID) -Konstruktormethode.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: CBaseFilter.CBaseFilter(const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) -Konstruktor (Amfilter.h)
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
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099828"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, \* CCritSec, REFCLSID) -Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseFilter(
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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Für das kritische Abschnittsobjekt würden Sie in der Regel einen der folgenden Schritte ausführen:

-   Leiten Sie eine Klasse ab, die sowohl **CBaseFilter** als auch **CCritSec** erbt. Übergeben Sie für *pLock* den `this` Zeiger.
-   Leiten Sie eine Klasse ab, die **CBaseFilter** erbt und eine **CCritSec-Membervariable** enthält. Übergeben Sie für *pLock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




