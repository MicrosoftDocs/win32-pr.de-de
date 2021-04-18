---
description: Die GetTypeInfoCount-Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Cbasedispatch. gettypanfocount-Methode (ctlutil. h)
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
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368422"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>Cbasedispatch. gettypanfocount-Methode

Die- `GetTypeInfoCount` Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.

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

Ein Zeiger auf eine Variable, die die Anzahl der vom-Objekt bereitgestellten Type-Information-Schnittstellen empfängt. Wenn die Methode zurückgibt, ist der Wert 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasedispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




