---
description: 'CBaseDispatch.GetTypeInfoCount-Methode: Die GetTypeInfoCount-Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt zur Verfügung stellt.'
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: CBaseDispatch.GetTypeInfoCount-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da80cdb4810ea3e598ad9483ccf52e8033ccb1a5b7ee65351e2cfcc273a3415f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660017"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>CBaseDispatch.GetTypeInfoCount-Methode

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseDispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




