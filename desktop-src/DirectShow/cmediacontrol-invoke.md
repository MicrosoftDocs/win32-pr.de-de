---
description: 'CMediaControl.Invoke-Methode: Ermöglicht den Zugriff auf Eigenschaften und Methoden, die von einem -Objekt verfügbar gemacht werden.'
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: CMediaControl.Invoke-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085638"
---
# <a name="cmediacontrolinvoke-method"></a>CMediaControl.Invoke-Methode

Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.

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

Bezeichner des Mitglieds. Verwenden [**Sie CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) oder die Dokumentation des Objekts, um den Dispatchbezeichner zu erhalten.

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

Flags, die den Kontext des Aufrufs `CMediaControl::Invoke` beschreiben.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Zeiger auf eine -Struktur, die ein Array von Argumenten, ein Array von Argument-Dispatch-IDs für benannte Argumente und die Anzahl der Elemente in den Arrays enthält.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Zeiger auf den Ort, an dem das Ergebnis gespeichert werden soll, oder **NULL,** wenn der Aufrufer kein Ergebnis erwartet.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Zeiger auf eine -Struktur, die Ausnahmeinformationen enthält.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Zeiger auf den Index des ersten Arguments innerhalb des **rgvarg-Arrays** der **DISPPARAMS-Struktur** mit einem Fehler. Weitere Informationen zu **DISPPARAMS finden** Sie im Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt DISP \_ E \_ UNKNOWNINTERFACE zurück, *wenn riid* nicht IID \_ NULL ist. Gibt einen der Fehlercodes von [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) zurück, wenn der Aufruf fehlschlägt. Andernfalls gibt das **HRESULT** aus dem Aufruf von **IDispatch::Invoke** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




