---
description: Die dobufferprocessingloop-Methode generiert Mediendaten und übergibt sie an die downstreameingabepin.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Csourcestream. dobufferprocessingloop-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351378"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>Csourcestream. dobufferprocessingloop-Methode

Die `DoBufferProcessingLoop` -Methode generiert Mediendaten und übergibt sie an die downstreameingabepin.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Der Thread hat eine Anforderung zum Abbrechen empfangen.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Stream wurde beendet, oder der Downstream-Filter akzeptiert keine Stichproben.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die Hauptschleife, die Daten verarbeitet und Sie nachgeschalteter Weise bereitstellt. Jedes Mal, wenn die-Schleife durchlaufen wird, ruft die-Methode ein leeres Medien Beispiel aus der Zuweisung ab. Sie übergibt das Beispiel an die [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode. Die **FillBuffer** -Methode, die von der abgeleiteten Klasse implementiert werden muss, generiert Mediendaten und platziert Sie im Beispiel Puffer.

Die Schleife wird beendet, wenn eine der folgenden Aktionen auftritt:

-   Die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der Eingabe-PIN lehnt ein Beispiel ab.
-   Die **FillBuffer** -Methode gibt S \_ false zurück, um das Ende des Streams anzugeben, oder gibt einen Fehlercode zurück.
-   Der Thread empfängt eine [**csourcestream:: Beendigung**](csourcestream-stop.md) -Anforderung.

Die- `DoBufferProcessingLoop` Methode verarbeitet das Ende der Stream-Benachrichtigung. Wenn ein Fehler auftritt, sendet er ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an den Filter Graph-Manager.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




