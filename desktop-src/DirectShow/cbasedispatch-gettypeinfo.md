---
description: Die GetTypeInfo-Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Cbasedispatch. gettypeingefo-Methode (ctlutil. h)
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
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369694"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Cbasedispatch. gettypeingefo-Methode

Die- `GetTypeInfo` Methode ruft die Typinformationen für das-Objekt ab, die dann zum Abrufen der Typinformationen für eine Schnittstelle verwendet werden können.

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

Verweis auf einen Schnittstellen Bezeichner (IID), der die-Schnittstelle angibt.

</dd> <dt>

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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode verhält sich wie die **IDispatch:: gettypeingefo** -Methode. Sie enthält jedoch den zusätzlichen Parameter *riid*, der die Schnittstelle angibt, für die Typinformationen abgerufen werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasedispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




