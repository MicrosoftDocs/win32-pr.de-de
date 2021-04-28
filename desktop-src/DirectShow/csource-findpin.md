---
description: 'CSource.FindPin-Methode: Die FindPin-Methode ruft den Pin mit dem angegebenen Bezeichner ab. Diese Methode implementiert die IBaseFilter::FindPin-Methode.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource.FindPin-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098858"
---
# <a name="csourcefindpin-method"></a>CSource.FindPin-Methode

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

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pin identifiziert.

</dd> <dt>

*ppPin* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IPin-Schnittstelle des Pins.**](/windows/desktop/api/Strmif/nn-strmif-ipin) Wenn die Methode fehlschlägt, \* *wird ppPin* auf NULL **festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                       | Beschreibung                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>         |  NULL-Zeigerargument.<br/>                 |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Eine Stecknadel mit diesem Bezeichner wurde nicht finden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der erste Pin hat immer den Namen "1". der zweite Pin heißt "2"; usw. Weitere Informationen finden Sie unter [**CSourceStream::QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




