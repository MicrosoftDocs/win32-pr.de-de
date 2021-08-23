---
description: 'CMediaPosition.GetTypeInfoCount-Methode: Die GetTypeInfoCount-Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt zur Verfügung stellt.'
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: CMediaPosition.GetTypeInfoCount-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 032584025d91d6e21b02ed74b26b2e59d55e3a6e044c215d586913d8417a412e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157008"
---
# <a name="cmediapositiongettypeinfocount-method"></a>CMediaPosition.GetTypeInfoCount-Methode

Die `GetTypeInfoCount` -Methode ruft die Anzahl der Schnittstellen mit Typinformationen ab, die das -Objekt bietet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pctinfo* 
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der vom -Objekt bereitgestellten Typinformationsschnittstellen empfängt. Wenn die Methode zurückgegeben wird, ist der Wert 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> |  NULL-Zeigerargument.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




