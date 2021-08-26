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
ms.openlocfilehash: f7d2f1b70202200c705394790bb4b1e8d81349b71f534cc36fba9a8baed65f03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998930"
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

Zeichenfolge, die den Namen des Objekts enthält; wird im [**CBaseObject-Konstruktor**](cbaseobject.md) für das Debuggen verwendet.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die IUnknown-Schnittstelle des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das -Objekt wird mit einem Verweiszähler von 0 (null) initialisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




