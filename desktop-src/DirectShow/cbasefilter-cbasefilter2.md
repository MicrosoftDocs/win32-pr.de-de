---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID) konstruktor - Constructor method.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: CBaseFilter.CBaseFilter(const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) konstruktor (Amfilter.h)
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
ms.openlocfilehash: 8455e78096af7bc2ca82a2b7634ceac14b2bdf6e918f62f8ae0fa64308f4b9a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640650"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, CCritSec, \* REFCLSID) konstruktor

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

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.

</dd> <dt>

*Clsid* 
</dt> <dd>

Klassenbezeichner (CLSID) des Filters.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




