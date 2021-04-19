---
description: Konstruktormethode.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Cbasinput PIN. cbasinput Pin-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366847"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a>Cbasinput PIN. cbasinput Pin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
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

*ppinname* 
</dt> <dd>

Breit Zeichen-Zeichenfolge, die den Pin-Namen (auch als PIN-Bezeichner verwendet) enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle Parameter werden direkt an den [**cbasepin**](cbasepin-cbasepin.md) -Konstruktor übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




