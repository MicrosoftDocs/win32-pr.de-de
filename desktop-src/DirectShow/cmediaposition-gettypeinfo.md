---
description: Die GetTypeInfo-Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Cmediaposition. GetTypeInfo-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361014"
---
# <a name="cmediapositiongettypeinfo-method"></a>Cmediaposition. GetTypeInfo-Methode

Die- `GetTypeInfo` Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*itinfo* 
</dt> <dd>

Typinformationen, die zurückgegeben werden. Muss Null sein.

</dd> <dt>

*lcid* 
</dt> <dd>

Gebietsschemabezeichner

</dd> <dt>

*pptinfo* 
</dt> <dd>

Adresse einer Variablen, die einen **itypeingefo** -Zeiger empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                             | Beschreibung                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeigerargument.<br/>          |
| <dl> <dt>**Geben Sie \_ E \_ elementnotfound ein.**</dt> </dl> | Der *itinfo* -Parameter ist nicht 0 (null).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaposition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




