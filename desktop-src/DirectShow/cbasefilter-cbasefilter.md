---
description: Konstruktormethode.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Cbasefilter. cbasefilter (Konst TCHAR *, LPUNKNOWN, ccritsec*, Ref CLSID, HRESULT *)-Konstruktor (amfilter. h)
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373756"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Cbasefilter. cbasefilter-Konstruktor (Konst TCHAR \* , LPUNKNOWN, ccritsec \* , Ref CLSID, HRESULT \* )

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

Zeiger auf eine Zeichenfolge, die den Namen des Filters für Debugzwecke enthält.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.

</dd> <dt>

*CLSID* 
</dt> <dd>

Klassen Bezeichner (CLSID) des Filters.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Der Konstruktor ignoriert diesen Parameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Für das Objekt "kritischer Abschnitt" würden Sie in der Regel eine der folgenden Aktionen ausführen:

-   Leiten Sie eine Klasse ab, die sowohl **cbasefilter** als auch **ccritsec** erbt. Übergeben Sie für *Plock* den- `this` Zeiger.
-   Leiten Sie eine Klasse ab, die **cbasefilter** erbt und eine **ccritsec** -Element Variable enthält. Übergeben Sie für *Plock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




