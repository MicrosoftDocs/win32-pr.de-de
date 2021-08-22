---
description: 'CMediaPosition.GetTypeInfo-Methode: Die GetTypeInfo-Methode ruft die Typinformationen für das Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.'
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
ms.openlocfilehash: 5a23632078fb4aa9b3aaa3f80c9c85ea5f8e0d0adfff49a057dc5b554f104fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832420"
---
# <a name="cmediapositiongettypeinfo-method"></a>CMediaPosition.GetTypeInfo-Methode

Die `GetTypeInfo` -Methode ruft die Typinformationen für das -Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.

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

Geben Sie informationen ein, die zurückgegeben werden sollen. Muss Null sein.

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
| <dl> <dt>**E \_ POINTER**</dt> </dl>               | **NULL-Zeigerargument.**<br/>          |
| <dl> <dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | Der *itinfo-Parameter* ist nicht 0 (null).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




