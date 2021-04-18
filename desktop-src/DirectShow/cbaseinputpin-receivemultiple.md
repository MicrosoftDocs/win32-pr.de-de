---
description: 'Die receivemultiple-Methode empfängt ein Array von-Beispielen. Diese Methode implementiert die IMemInputPin:: receivemultiple-Methode.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Cbaseinputpin. receivemultiple-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364535"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Cbaseinputpin. receivemultiple-Methode

Die- `ReceiveMultiple` Methode empfängt ein Array von-Beispielen. Diese Methode implementiert die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psamples* 
</dt> <dd>

Die Adresse eines Arrays von [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeigern der Größe *nsamples*.

</dd> <dt>

*nsamples* 
</dt> <dd>

Anzahl der zu verarbeitenden Stichproben.

</dd> <dt>

*nsamplesprocgelassene* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der verarbeiteten Beispiele empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                             | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeigerargument.<br/>                      |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Ungültiger Medientyp.<br/>                             |
| <dl> <dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt> </dl>   | Laufzeitfehler.<br/>                      |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>     | Die PIN wurde beendet.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode verhält sich wie die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode, empfängt jedoch ein Array von Beispielen. In der Basisklasse durchläuft die-Methode das Array und ruft mit jedem Beispiel **Receive** auf. Überschreiben Sie diese Funktion, wenn der Filter Batches von Beispielen effizienter verarbeiten kann, als Sie nacheinander verarbeitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




