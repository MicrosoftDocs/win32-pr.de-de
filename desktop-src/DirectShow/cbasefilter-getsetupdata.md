---
description: Die getsetupdata-Methode ruft die Registrierungsdaten für den Filter ab.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Cbasefilter. getsetupdata-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367756"
---
# <a name="cbasefiltergetsetupdata-method"></a>Cbasefilter. getsetupdata-Methode

Die- `GetSetupData` Methode ruft die Registrierungsdaten für den Filter ab.

> [!Note]  
> Diese Methode ist veraltet. Sie wird von den Methoden [**cbasefilter:: Register**](cbasefilter-register.md) und [**cbasefilter:: unregister**](cbasefilter-unregister.md) aufgerufen.

 

## <a name="syntax"></a>Syntax


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur zurück, die Registrierungsinformationen für den Filter enthält.

## <a name="remarks"></a>Bemerkungen

Die Basisklasse gibt **null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




