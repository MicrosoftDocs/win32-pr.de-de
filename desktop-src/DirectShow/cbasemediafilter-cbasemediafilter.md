---
description: Konstruktormethode.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Cbasemediafilter. cbasemediafilter-Konstruktor (amfilter. h)
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
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351220"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Cbasemediafilter. cbasemediafilter-Konstruktor

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

Klassen Bezeichner des-Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein anderes Objekt das Objekt enthält oder aggregiert `CBaseMediaFilter` , kann die **ccritsec** -Sperre für das Objekt extern sein `CBaseMediaFilter` . Übergeben Sie in diesem Fall einen Zeiger auf die Sperre in *Plock*.

Andernfalls können Sie folgende Aktionen ausführen:

-   Leiten Sie eine Klasse ab, die sowohl `CBaseMediaFilter` als auch **ccritsec** erbt. Übergeben Sie für *Plock* den this-Zeiger.
-   Leiten Sie eine Klasse ab, die erbt `CBaseMediaFilter` und eine **ccritsec** -Element Variable enthält. Übergeben Sie für *Plock* die Adresse dieser Variablen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




