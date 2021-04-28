---
description: 'CMediaPosition.GetTypeInfoCount-Methode: Die GetTypeInfoCount-Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das Objekt bereitstellt.'
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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095478"
---
# <a name="cmediapositiongettypeinfocount-method"></a>CMediaPosition.GetTypeInfoCount-Methode

Die `GetTypeInfoCount` -Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das -Objekt bereitstellt.

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
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerargument.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




