---
description: Die crendererinputpin-Methode ist eine Konstruktormethode.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Crendererinputpin. crendererinputpin-Konstruktor (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372491"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Crendererinputpin. crendererinputpin-Konstruktor

Die- `CRendererInputPin` Methode ist eine Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prenderer* 
</dt> <dd>

Zeiger auf das [**cbaserenderer**](cbaserenderer.md) -Objekt, das den Filter implementiert.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt.

</dd> <dt>

*Name* 
</dt> <dd>

Zeiger auf eine breit Zeichen-Zeichenfolge, die den PIN-Bezeichner enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




