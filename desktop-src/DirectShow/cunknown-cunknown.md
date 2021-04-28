---
description: 'CUnknown.CUnknown-Konstruktor : Konstruktormethode.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: CUnknown.CUnknown-Konstruktor (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084608"
---
# <a name="cunknowncunknown-constructor"></a>CUnknown.CUnknown-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen des Objekts enthält. wird im [**CBaseObject-Konstruktor zum**](cbaseobject.md) Debuggen verwendet.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die IUnknown-Schnittstelle des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das -Objekt wird mit einem Verweiszähler von 0 (null) initialisiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




