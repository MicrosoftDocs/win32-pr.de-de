---
description: Die CBaseOutputPin-Klasse ist eine abstrakte Basisklasse, die einen Ausgabepin implementiert.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: CBaseOutputPin-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a4051f904b27b75273d553e1d0604b068b3910fbfb322b5a2df716c996a1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872585"
---
# <a name="cbaseoutputpin-class"></a>CBaseOutputPin-Klasse

![cbaseoutputpin-Klassenhierarchie](images/filter06.png)

Die `CBaseOutputPin` -Klasse ist eine abstrakte Basisklasse, die einen Ausgabepin implementiert.

Diese Klasse wird von [**CBasePin ableiten.**](cbasepin.md) Sie unterscheidet **sich von CBasePin** in folgenden Hinsicht:

-   Es wird nur eine Verbindung mit Eingabepins herstellt, die die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) unterstützen.
-   Er unterstützt den lokalen Speichertransport über die [**IMemAllocator-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)
-   Sie lehnt Benachrichtigungen zum Ende des Streams, zum Leeren und zu neuen Segmenten ab. (Diese sollten nicht an einen Ausgabepin gesendet werden.)
-   Es stellt Methoden für die Nachverarbeitung von Beispielen zur Verfügung.

Wenn der Pin eine Verbindung herstellt, fordert er eine Speicherzuweisung vom Eingabepin an. Wenn dies nicht der Fehler ist, wird ein neues Zuweisungsobjekt erstellt. Der Ausgabepin ist für das Festlegen der Zuweisungseigenschaften verantwortlich. Dies wird mit der reinen virtuellen [**Methode CBaseOutputPin::D ecideBufferSize ausgeführt.**](cbaseoutputpin-decidebuffersize.md) Überschreiben Sie diese Methode in der abgeleiteten Klasse. Wenn der Eingabepin Pufferanforderungen hat, werden sie an die **DecideBufferSize-Methode** übergeben.

Rufen Sie [**die CBaseOutputPin::GetDeliveryBuffer-Methode**](cbaseoutputpin-getdeliverybuffer.md) auf, um ein leeres Medienbeispiel zu erhalten. Rufen Sie [**die CBaseOutputPin::D eliver-Methode**](cbaseoutputpin-deliver.md) auf, um Nachgelagerte Beispiele zu liefern.

Die abgeleitete Klasse muss die rein virtuelle [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) überschreiben, um den Medientyp während pin-Verbindungen zu überprüfen.



| Geschützte Membervariablen                                      | Beschreibung                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | Zeiger auf die Speicherzuweisung.                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | Zeiger auf den Eingabepin, der mit diesem Pin verbunden ist.                            |
| Öffentliche Methoden                                                  | Beschreibung                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Konstruktormethode.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Schließt eine Verbindung mit einem Eingabepin ab. Virtuellen.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Wählt eine Speicherzuweisung aus. Virtuellen.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Ruft ein Medienbeispiel ab, das einen leeren Puffer enthält. Virtuellen.           |
| [**Bereitstellen**](cbaseoutputpin-deliver.md)                       | Übergibt ein Medienbeispiel an den verbundenen Eingabepin. Virtuellen.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Erstellt eine Speicherzuweisung. Virtuellen.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Bestimmt, ob eine Stecknadelverbindung geeignet ist.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Gibt den Pin von einer Verbindung frei.                                        |
| [**Aktiv**](cbaseoutputpin-active.md)                         | Benachrichtigt den Pin, dass der Filter jetzt aktiv ist.                            |
| [**Inaktiv**](cbaseoutputpin-inactive.md)                     | Benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Übergibt eine Benachrichtigung am Ende des Streams an den verbundenen Eingabepin. Virtuellen. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten. Virtuellen.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden. Virtuellen.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Übergibt eine Benachrichtigung für ein neues Segment an den verbundenen Eingabepin. Virtuellen.   |
| Rein virtuelle Methoden                                            | Beschreibung                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Legt die Pufferanforderungen fest.                                              |
| IPin-Methoden                                                    | Beschreibung                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Startet einen Leerungsvorgang.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Beendet einen Leerungsvorgang.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden.                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




