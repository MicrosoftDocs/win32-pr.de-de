---
description: Die cbaseoutputpin-Klasse ist eine abstrakte Basisklasse, die eine Ausgabe-PIN implementiert.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Cbaseoutputpin-Klasse (amfilter. h)
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
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365543"
---
# <a name="cbaseoutputpin-class"></a>Cbaseoutputpin-Klasse

![cbaseoutputpin-Klassenhierarchie](images/filter06.png)

Die- `CBaseOutputPin` Klasse ist eine abstrakte Basisklasse, die eine Ausgabe-PIN implementiert.

Diese Klasse wird von [**cbasepin**](cbasepin.md)abgeleitet. Dies unterscheidet sich von **cbasepin** in den folgenden Punkten:

-   Es stellt nur eine Verbindung mit Eingabe Pins her, die die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle unterstützen.
-   Es unterstützt den lokalen Speicher Transport über die [**imembelegcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle.
-   Er lehnt Streamende-, Lösch-und neue Segment Benachrichtigungen ab. (Diese sollten nicht an eine Ausgabepin gesendet werden.)
-   Es stellt Methoden zum Bereitstellen von Abtastungen bereit.

Wenn die PIN eine Verbindung herstellt, wird von der eingabepin eine Speicherzuweisung angefordert. Wenn ein Fehler auftritt, wird ein neues zuordnerobjekt erstellt. Die Ausgabepin ist für das Festlegen der zuweicatoreigenschaften verantwortlich. Dies erfolgt über die reine virtuelle Methode [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md). Überschreiben Sie diese Methode in der abgeleiteten Klasse. Wenn die Eingabe-PIN beliebige Puffer Anforderungen hat, werden Sie an die **decidebuffersize** -Methode übergeben.

Rufen Sie die [**cbaseoutputpin:: getdeliverybuffer**](cbaseoutputpin-getdeliverybuffer.md) -Methode auf, um ein leeres Medien Beispiel zu erhalten. Rufen Sie die [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md) -Methode auf, um Abtastungen übermitteln.

Ihre abgeleitete Klasse muss die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode überschreiben, um den Medientyp während der PIN-Verbindungen zu überprüfen.



| Geschützte Member-Variablen                                      | BESCHREIBUNG                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m- \_ pallocator**](cbaseoutputpin-m-pallocator.md)            | Zeiger auf die Speicherzuweisung.                                           |
| [**m \_ pinputpin**](cbaseoutputpin-m-pinputpin.md)              | Zeiger auf die Eingabe-PIN, die mit dieser Pin verbunden ist.                            |
| Öffentliche Methoden                                                  | BESCHREIBUNG                                                                |
| [**Cbaseoutputpin**](cbaseoutputpin-cbaseoutputpin.md)         | Konstruktormethode.                                                        |
| [**Completeconnect**](cbaseoutputpin-completeconnect.md)       | Schließt eine Verbindung mit einer Eingabe-PIN ab. Virtu.                           |
| [**Decidezuordcator**](cbaseoutputpin-decideallocator.md)       | Wählt eine Speicherzuweisung aus. Virtu.                                       |
| [**Getdeliverybuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Ruft ein Medien Beispiel ab, das einen leeren Puffer enthält. Virtu.           |
| [**Bereitstellen**](cbaseoutputpin-deliver.md)                       | Übermittelt ein Medien Beispiel an die verbundene Eingabe-PIN. Virtu.               |
| [**Initzuweisung**](cbaseoutputpin-initallocator.md)           | Erstellt eine Speicherzuweisung. Virtu.                                       |
| [**Check Connect**](cbaseoutputpin-checkconnect.md)             | Bestimmt, ob eine PIN-Verbindung geeignet ist.                           |
| [**Breakconnect**](cbaseoutputpin-breakconnect.md)             | Gibt die PIN von einer Verbindung frei.                                        |
| [**Aktiv**](cbaseoutputpin-active.md)                         | Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.                            |
| [**Inaktiv**](cbaseoutputpin-inactive.md)                     | Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.                      |
| [**Deliverendof**](cbaseoutputpin-deliverendofstream.md) | Übermittelt eine Benachrichtigung über das Ende des Streams an die verbundene Eingabe-PIN. Virtu. |
| [**Deliverbeginflush**](cbaseoutputpin-deliverbeginflush.md)   | Fordert an, dass die verbundene Eingabe-PIN einen Leerungs Vorgang startet. Virtu.      |
| [**Deliverendflush**](cbaseoutputpin-deliverendflush.md)       | Fordert die verbundene Eingabe-PIN an, einen Leerungs Vorgang zu beenden. Virtu.        |
| [**Delivernewsegment**](cbaseoutputpin-delivernewsegment.md)   | Übermittelt eine Benachrichtigung über ein neues Segment an die verbundene Eingabe-PIN. Virtu.   |
| Reine virtuelle Methoden                                            | BESCHREIBUNG                                                                |
| [**Decidebuffersize**](cbaseoutputpin-decidebuffersize.md)     | Legt die Puffer Anforderungen fest.                                              |
| IPin-Methoden                                                    | BESCHREIBUNG                                                                |
| [**Beginflush**](cbaseoutputpin-beginflush.md)                 | Startet einen Löschvorgang.                                                  |
| [**Endflush**](cbaseoutputpin-endflush.md)                     | Beendet einen Löschvorgang.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




