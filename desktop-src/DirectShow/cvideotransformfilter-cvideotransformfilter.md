---
description: Konstruktormethode.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Cvideotransformfilter. cvideotransformfilter-Konstruktor (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360980"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a>Cvideotransformfilter. cvideotransformfilter-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeichenfolge, die den debugnamen des Filters enthält. Weitere Informationen finden Sie unter [**cbaseobject:: cbaseobject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*CLSID* 
</dt> <dd>

Klassen Bezeichner des Filters.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




