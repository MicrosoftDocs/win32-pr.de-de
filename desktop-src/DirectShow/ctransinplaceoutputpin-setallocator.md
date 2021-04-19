---
description: Die Methode "Methode" gibt eine Zuweisung für die Verbindung an.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Ctransinplaceoutputpin. log-Locator-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370015"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>Ctransinplaceoutputpin. log-Locator-Methode

Die- `SetAllocator` Methode gibt eine Zuweisung für die Verbindung an.

## <a name="syntax"></a>Syntax


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pallocator* 
</dt> <dd>

Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Ausgabe-PIN für diesen Filter stellt nie eine Zuweisung bereit. Diese Methode gibt die Zuweisung für die Ausgabepin an. Er legt den Wert der [**cbaseoutputpin:: m \_ pallocator**](cbaseoutputpin-m-pallocator.md) -Member-Variable fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceoutputpin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




