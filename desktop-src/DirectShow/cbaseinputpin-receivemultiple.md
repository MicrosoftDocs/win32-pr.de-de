---
description: Die ReceiveMultiple-Methode empfängt ein Array von Beispielen. Diese Methode implementiert die IMemInputPin::ReceiveMultiple-Methode.
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: CBaseInputPin.ReceiveMultiple-Methode (Amfilter.h)
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
ms.openlocfilehash: 63d71f47978a2eefdcbdacbe1c31bfe69c732c24a0479357b35aa1ddd2b0a9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079400"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>CBaseInputPin.ReceiveMultiple-Methode

Die `ReceiveMultiple` -Methode empfängt ein Array von Stichproben. Diese Methode implementiert die [**IMemInputPin::ReceiveMultiple-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)

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

*pSamples* 
</dt> <dd>

Adresse eines Arrays von [**IMediaSample-Zeigern**](/windows/desktop/api/Strmif/nn-strmif-imediasample) der Größe *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Anzahl der zu verarbeitenden Beispiele.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der verarbeiteten Stichproben empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                             | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Pin wird gerade geleert. Das Beispiel wurde abgelehnt.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>               |  NULL-Zeigerargument.<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Ungültiger Medientyp.<br/>                             |
| <dl> <dt>**VFW \_ \_ E-LAUFZEITFEHLER \_**</dt> </dl>   | Es ist ein Laufzeitfehler aufgetreten.<br/>                      |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl>     | Die Stecknadel wird beendet.<br/>                             |



 

## <a name="remarks"></a>Hinweise

Diese Methode verhält sich wie die [**CBaseInputPin::Receive-Methode,**](cbaseinputpin-receive.md) empfängt jedoch ein Array von Beispielen. In der Basisklasse durchfing die -Methode das Array und ruft **Receive mit** jedem Beispiel auf. Überschreiben Sie diese Funktion, wenn Ihr Filter Batches von Stichproben effizienter verarbeiten kann, als sie nach und nach zu verarbeiten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




