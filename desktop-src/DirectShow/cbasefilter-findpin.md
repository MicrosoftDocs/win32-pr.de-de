---
description: 'CBaseFilter.FindPin-Methode: Die FindPin-Methode ruft den Pin mit dem angegebenen Bezeichner ab. Diese Methode implementiert die IBaseFilter::FindPin-Methode.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: CBaseFilter.FindPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099818"
---
# <a name="cbasefilterfindpin-method"></a>CBaseFilter.FindPin-Methode

Die `FindPin` -Methode ruft den Pin mit dem angegebenen Bezeichner ab. Diese Methode implementiert die [**IBaseFilter::FindPin-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

## <a name="syntax"></a>Syntax


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Zeiger auf eine konstante, mit NULL endende Unicode-Zeichenfolge, die den Pin identifiziert.

</dd> <dt>

*ppPin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                       | Beschreibung                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>         | **NULL-Zeigerargument.**<br/>     |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Ein übereinstimmender Pin wurde nicht gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**CBasePin::Name-Methode**](cbasepin-name.md) auf, um den Namen jedes Pins mit der zeichenfolge zu vergleichen, die durch den *Id-Parameter* angegeben wird.

Wenn die Methode erfolgreich ist, verfügt die **IPin-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




