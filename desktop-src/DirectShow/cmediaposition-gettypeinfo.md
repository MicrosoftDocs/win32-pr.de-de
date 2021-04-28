---
description: 'CMediaPosition.GetTypeInfo-Methode: Die GetTypeInfo-Methode ruft die Typinformationen für das Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: CMediaPosition.GetTypeInfo-Methode (Ctlutil.h)
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099138"
---
# <a name="cmediapositiongettypeinfo-method"></a>CMediaPosition.GetTypeInfo-Methode

Die `GetTypeInfo` -Methode ruft die Typinformationen für das -Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.

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

Geben Sie informationen ein, die sie zurückgeben. Muss Null sein.

</dd> <dt>

*lcid* 
</dt> <dd>

Gebietsschemabezeichner

</dd> <dt>

*pptinfo* 
</dt> <dd>

Adresse einer Variablen, die einen **ITypeInfo-Zeiger** empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                             | Beschreibung                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                            |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>               |  NULL-Zeigerargument.<br/>          |
| <dl> <dt>**TYP \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Der *itinfo-Parameter* ist nicht 0 (null).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




