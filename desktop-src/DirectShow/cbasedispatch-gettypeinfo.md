---
description: 'CBaseDispatch.GetTypeInfo-Methode: Die GetTypeInfo-Methode ruft die Typinformationen für das Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.'
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: CBaseDispatch.GetTypeInfo-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076680"
---
# <a name="cbasedispatchgettypeinfo-method"></a>CBaseDispatch.GetTypeInfo-Methode

Die `GetTypeInfo` -Methode ruft die Typinformationen für das -Objekt ab, die dann verwendet werden können, um die Typinformationen für eine Schnittstelle abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* 
</dt> <dd>

Verweis auf einen Schnittstellenbezeichner (IID), der die Schnittstelle angibt.

</dd> <dt>

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



 

## <a name="remarks"></a>Hinweise

Diese Methode verhält sich wie die **IDispatch::GetTypeInfo-Methode.** Sie enthält jedoch einen zusätzlichen Parameter, *riid,* der die Schnittstelle angibt, für die Typinformationen abgerufen werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseDispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




