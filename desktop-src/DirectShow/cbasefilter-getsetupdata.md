---
description: Die GetSetupData-Methode ruft die Registrierungsdaten für den Filter ab.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: CBaseFilter.GetSetupData-Methode (Amfilter.h)
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
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640470"
---
# <a name="cbasefiltergetsetupdata-method"></a>CBaseFilter.GetSetupData-Methode

Die `GetSetupData` -Methode ruft die Registrierungsdaten für den Filter ab.

> [!Note]  
> Diese Methode ist veraltet. Sie wird von den [**Methoden CBaseFilter::Register**](cbasefilter-register.md) und [**CBaseFilter::Unregister**](cbasefilter-unregister.md) aufgerufen.

 

## <a name="syntax"></a>Syntax


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**AMOVIESETUP \_ FILTER-Struktur zurück,**](amoviesetup-filter.md) die Registrierungsinformationen für den Filter enthält.

## <a name="remarks"></a>Hinweise

Die Basisklasse gibt **NULL zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




