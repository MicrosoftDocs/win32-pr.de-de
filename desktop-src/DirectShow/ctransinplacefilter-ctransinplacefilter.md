---
description: 'CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor : Konstruktormethode.'
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084778"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen des Filters enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Klassenbezeichner des Filters.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Filter die Eingabedaten ändert. True **gibt an,** dass der Filter die Daten ändert. Andernfalls übergibt der Filter die Daten unverändert nachgelagert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




