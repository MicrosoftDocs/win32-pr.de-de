---
description: 'Ordnet eine einzelne Element Funktion und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der cmediaevent:: aufrufen-Member-Funktion verwendet werden kann.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Cmediaevent. GetIDsOfNames-Methode (ctlutil. h)
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
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361015"
---
# <a name="cmediaeventgetidsofnames-method"></a>Cmediaevent. GetIDsOfNames-Methode

Ordnet eine einzelne Element Funktion und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der [**cmediaevent:: Aufrufen**](cmediaevent-invoke.md) -Member-Funktion verwendet werden kann.

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

Verweis Bezeichner. Für die zukünftige Verwendung reserviert. Muss **null** sein.

</dd> <dt>

*rgsznames* 
</dt> <dd>

Adresse eines Zeigers auf ein zugeordnetes Array von Namen, die zugeordnet werden sollen.

</dd> <dt>

*CNAMES* 
</dt> <dd>

Die Anzahl der zuzuordnenden Namen.

</dd> <dt>

*lcid* 
</dt> <dd>

Der Gebiets Schema Kontext, in dem die Namen interpretiert werden sollen.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Zeiger auf ein Array, das vom Aufrufer zugeordnet wird. jedes Element von enthält eine ID, die einem der Namen entspricht, die im *rgsznames* -Array übergeben werden. Das erste Element stellt den Elementnamen dar. die nachfolgenden Elemente stellen jeden der Parameter des Members dar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ E \_ unbekannte \_ CLSID**</dt> </dl> | Die CLSID wurde nicht erkannt.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ unknownname**</dt> </dl>    | Mindestens ein Name ist nicht bekannt. Die zurückgegebenen DispIds enthalten \_ für jeden Eintrag, der einem unbekannten Namen entspricht, die DISPID unbekannt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>          | Nicht genügend Arbeitsspeicher.<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaevent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




