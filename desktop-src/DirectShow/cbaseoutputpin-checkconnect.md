---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Cbaseoutputpin. checkConnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368600"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Cbaseoutputpin. checkConnect-Methode

Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                               | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                                                         |
| <dl> <dt>**E \_ nointerface**</dt> </dl>             | Die eingabepin unterstützt [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)nicht.<br/> |
| <dl> <dt>**VFW \_ E \_ ungültige \_ Richtung**</dt> </dl> | PIN-Anweisungen sind nicht kompatibel.<br/>                               |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode der Basisklasse auf und fragt dann die Eingabe-PIN für Ihre [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




