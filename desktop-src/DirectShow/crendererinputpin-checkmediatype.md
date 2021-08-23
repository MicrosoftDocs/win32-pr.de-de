---
description: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. Diese Methode überschreibt die CBasePin::CheckMediaType-Methode.
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: CRendererInputPin.CheckMediaType-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d47f69c72ab2dab366b42d6dc80100508c0b1608d25abdcbfb1bb49c4177a278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687700"
---
# <a name="crendererinputpincheckmediatype-method"></a>CRendererInputPin.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. Diese Methode überschreibt die [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein Medientypobjekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRendererInputPin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




