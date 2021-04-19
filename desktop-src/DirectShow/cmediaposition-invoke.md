---
description: Die Aufruf Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Cmediaposition. aufrufen-Methode (ctlutil. h)
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
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366880"
---
# <a name="cmediapositioninvoke-method"></a>Cmediaposition. aufrufen-Methode

Die- `Invoke` Methode ermöglicht den Zugriff auf Eigenschaften und Methoden, die vom-Objekt verfügbar gemacht werden.

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

*dispidmember* 
</dt> <dd>

Der Bezeichner des Members. Verwenden Sie [**cmediaposition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) , um den Dispatchbezeichner abzurufen.

</dd> <dt>

*riid* 
</dt> <dd>

Für die zukünftige Verwendung reserviert. Muss IID \_ NULL sein.

</dd> <dt>

*lcid* 
</dt> <dd>

Der Gebiets Schema Kontext, in dem Argumente interpretiert werden sollen.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flags, die den Kontext des Aufrufs beschreiben.

</dd> <dt>

*pdispparameams* 
</dt> <dd>

Zeiger auf eine **dipparams** -Struktur, die die Argumente enthält.

</dd> <dt>

*pVarResult* 
</dt> <dd>

Zeiger auf eine **Variante** , die das Ergebnis empfängt, oder **null** , wenn der Aufrufer kein Ergebnis erwartet.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die Ausnahme Informationen empfängt.

</dd> <dt>

*gibt puArgErr* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Index des ersten Arguments empfängt, das einen Fehler verursacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                              |
| <dl> <dt>**DISP \_ E \_ unknowninterface**</dt> </dl> | Der *riid* -Parameter ist nicht IID \_ NULL.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaposition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




