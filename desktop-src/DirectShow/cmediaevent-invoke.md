---
description: Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Cmediaevent. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22482cffe11f62d50361bc950409858a2436d8a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358742"
---
# <a name="cmediaeventinvoke-method"></a>Cmediaevent. aufrufen-Methode

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

*dispidmember* 
</dt> <dd>

Der Bezeichner des Members. Verwenden Sie [**cmediaevent:: GetIDsOfNames**](cmediaevent-getidsofnames.md) oder die Dokumentation des Objekts, um den Dispatchbezeichner abzurufen.

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

Flags, die den Kontext des `CMediaEvent::Invoke` Aufrufes beschreiben.

</dd> <dt>

*pdispparameams* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die ein Array von Argumenten, ein Array von Argument dispatchids für benannte Argumente und Zähler für die Anzahl der Elemente in den Arrays enthält.

</dd> <dt>

*pVarResult* 
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem das Ergebnis gespeichert werden soll, oder **null** , wenn der Aufrufer kein Ergebnis erwartet.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Zeiger auf eine-Struktur, die Ausnahme Informationen enthält.

</dd> <dt>

*gibt puArgErr* 
</dt> <dd>

Zeiger auf den Index des ersten Arguments innerhalb des **rgvarg** -Arrays der **DISPPARAMS** -Struktur, das einen Fehler aufweist. Weitere Informationen zu **disppara** Metern finden Sie unter Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt DISP \_ E \_ unknowninterface zurück, wenn *riid* nicht IID \_ NULL ist. Gibt einen der Fehlercodes aus [**cmediaevent:: GetTypeInfo**](cmediaevent-gettypeinfo.md) zurück, wenn der-Rückruf fehlschlägt. Andernfalls wird das **HRESULT** aus dem Aufruf von **IDispatch::** Aufruf zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaevent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




