---
description: Karten eine einzelne Memberfunktion und einen optionalen Satz von Parametern zu einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern, die bei nachfolgenden Aufrufen der CMediaEvent::Invoke-Memberfunktion verwendet werden können.
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: CMediaEvent.GetIDsOfNames-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a638861bc6a01a615355f0fad05cddc00f31d3e659fc60c0be0246eb108583f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401873"
---
# <a name="cmediaeventgetidsofnames-method"></a>CMediaEvent.GetIDsOfNames-Methode

Karten eine einzelne Memberfunktion und einen optionalen Satz von Parametern zu einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern, die bei nachfolgenden Aufrufen der [**CMediaEvent::Invoke-Memberfunktion**](cmediaevent-invoke.md) verwendet werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* 
</dt> <dd>

Verweisbezeichner. Für die zukünftige Verwendung reserviert. Muss **NULL** sein.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Adresse eines Zeigers auf ein übergebenes Array von Namen, die zugeordnet werden sollen.

</dd> <dt>

*cNames* 
</dt> <dd>

Die Anzahl der zuzuordnenden Namen.

</dd> <dt>

*lcid* 
</dt> <dd>

Gebietsschemakontext, in dem die Namen interpretiert werden sollen.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Zeiger auf ein vom Aufrufer zugeordnetes Array, von dem jedes Element eine ID enthält, die einem der im *rgszNames-Array übergebenen Namen entspricht.* Das erste Element stellt den Elementnamen dar. die nachfolgenden Elemente stellen jeden Parameter des Members dar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ E \_ UNKNOWN \_ CLSID**</dt> </dl> | Die CLSID wurde nicht erkannt.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl>    | Mindestens ein Name war nicht bekannt. Die zurückgegebenen DISPIDs enthalten DISPID UNKNOWN für jeden Eintrag, der \_ einem unbekannten Namen entspricht.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Nicht genügend Arbeitsspeicher.<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaEvent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




