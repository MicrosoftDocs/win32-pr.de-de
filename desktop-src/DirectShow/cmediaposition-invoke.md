---
description: Die Invoke-Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom -Objekt verfügbar gemacht werden.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: CMediaPosition.Invoke-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dac439b94a62e9dbd11ca9e12ab80023071fc00cf22abcf6b9b4b93b07c356c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156856"
---
# <a name="cmediapositioninvoke-method"></a>CMediaPosition.Invoke-Methode

Die `Invoke` -Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom -Objekt verfügbar gemacht werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dispidMember* 
</dt> <dd>

Bezeichner des Mitglieds. Verwenden [**Sie CMediaPosition::GetIDsOfNames,**](cmediaposition-getidsofnames.md) um den Dispatchbezeichner zu erhalten.

</dd> <dt>

*riid* 
</dt> <dd>

Für die zukünftige Verwendung reserviert. Muss IID NULL \_ sein.

</dd> <dt>

*lcid* 
</dt> <dd>

Der Locale-Kontext, in dem Argumente interpretiert werden.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flags, die den Kontext des Aufrufs beschreiben.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Zeiger auf eine **DIPPARAMS-Struktur,** die die Argumente enthält.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Zeiger auf  einen VARIANT-Wert, der das Ergebnis empfängt, oder **NULL,** wenn der Aufrufer kein Ergebnis erwartet.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Zeiger auf eine -Struktur, die Ausnahmeinformationen empfängt.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Zeiger auf eine Variable, die den Index des ersten Arguments empfängt, das einen Fehler verursacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | Der *riid-Parameter* ist nicht IID \_ NULL.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




