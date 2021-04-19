---
description: Konstruktormethode.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Cbaseoutputpin. cbaseoutputpin-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371502"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>Cbaseoutputpin. cbaseoutputpin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobjectname* 
</dt> <dd>

Zeichenfolge, die den debugnamen des-Objekts enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diese Pin erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden. Dabei kann es sich um denselben kritischen Abschnitt handeln wie die Filter Sperre, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.

</dd> <dt>

*pName* 
</dt> <dd>

Breit Zeichen-Zeichenfolge, die den Pin-Namen (auch als PIN-Bezeichner verwendet) enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle Parameter werden direkt an den [**cbasepin**](cbasepin.md) -Konstruktor übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




