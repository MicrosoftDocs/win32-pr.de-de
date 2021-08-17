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
ms.openlocfilehash: 3818ef4356f11a2d003abe4e9442c4de06108aa32e50f480a3d097ea5db0c343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017188"
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

Zeiger auf eine konstante, mit NULL beendete Unicode-Zeichenfolge, die den Pin identifiziert.

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
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>         |  NULL-Zeigerargument.<br/>     |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Es wurde kein passender Pin finden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBasePin::Name-Methode**](cbasepin-name.md) auf, um den Namen jedes Pins mit der durch den Id-Parameter angegebenen *Zeichenfolge zu* vergleichen.

Wenn die Methode erfolgreich ist, verfügt die **IPin-Schnittstelle** über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie sie veröffentlichen, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




