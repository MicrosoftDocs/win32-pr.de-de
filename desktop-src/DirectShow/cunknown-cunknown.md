---
description: Konstruktormethode.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Cunknown. cunknown-Konstruktor (ComBase. h)
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
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356386"
---
# <a name="cunknowncunknown-constructor"></a>Cunknown. cunknown-Konstruktor

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

Zeichenfolge, die den Namen des Objekts enthält. wird im [**cbaseobject**](cbaseobject.md) -Konstruktor für das Debuggen verwendet.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die IUnknown-Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Objekt wird mit einem Verweis Zähler von NULL initialisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




