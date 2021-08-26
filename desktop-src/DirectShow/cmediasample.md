---
description: Die CMediaSample-Klasse definiert ein Medienbeispiel, das die IMediaSample2-Schnittstelle unterstützt. Das Medienbeispiel enthält einen Zeiger auf einen Speicherpuffer und verschiedene Eigenschaften, die als geschützte Membervariablen gespeichert sind.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: CMediaSample-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b0b27c8878a2841eeecb3bc1ae24bdcc43d056c57a881596179f5d2bd990fcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084490"
---
# <a name="cmediasample-class"></a>CMediaSample-Klasse

![cmediasample-Klassenhierarchie](images/wutil03.png)

Die `CMediaSample` -Klasse definiert ein Medienbeispiel, das die [**IMediaSample2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) unterstützt. Das Medienbeispiel enthält einen Zeiger auf einen Speicherpuffer und verschiedene Eigenschaften, die als geschützte Membervariablen gespeichert sind.

Medienbeispiele werden von Zuweisungen erstellt, die von der [**CBaseAllocator-Klasse**](cbaseallocator.md) abgeleitet werden. Der `CMediaSample` Konstruktor empfängt einen Zeiger auf einen zugeordneten Puffer zusammen mit der Größe des Puffers. Andere Eigenschaften werden in der Regel über [**IMediaSample-Schnittstellenmethoden**](/windows/desktop/api/Strmif/nn-strmif-imediasample) festgelegt und abgerufen.

Der Lebenszyklus eines Medienbeispiels unterscheidet sich von dem der meisten COM-Objekte:

-   Die Zuweisung enthält eine Liste kostenloser Beispiele. Wenn ein Filter ein neues Beispiel benötigt, ruft er die [**IMemAllocator::GetBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) der Zuweisung auf. Die Zuweisung ruft eine Stichprobe aus der freien Liste ab, erhöht den Verweiszähler der Stichprobe und gibt einen Zeiger auf die Stichprobe zurück.
-   Nachdem der Filter mit dem Beispiel abgeschlossen wurde, ruft er die **IUnknown::Release-Methode** für das Beispiel auf. Im Gegensatz zu den meisten Objekten löscht sich das Beispiel nicht selbst, wenn der Verweiszähler 0 (null) erreicht. Stattdessen ruft sie die [**IMemAllocator::ReleaseBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) für die Zuweisung auf, und die Zuweisung gibt das Beispiel an die freie Liste zurück.
-   Die Zuweisung zerstört stichprobenweise erst, wenn die [**IMemAllocator::D ecommit-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) aufgerufen wird.



| Geschützte Membervariablen                                           | BESCHREIBUNG                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Beispieleigenschaftenflags.                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | Typspezifische Flags.                                                                            |
| [**m \_ pBuffer**](cmediasample-m-pbuffer.md)                         | Zeiger auf den Speicherpuffer, der die Mediendaten enthält.                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | Länge der gültigen Daten im Puffer in Bytes.                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | Größe des Puffers in Bytes.                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Zeiger auf das nächste Beispiel in der Liste der Beispiele der Zuweisung.                                  |
| [**m \_ Start**](cmediasample-m-start.md)                             | Beispielstartzeit.                                                                              |
| [**m \_ Ende**](cmediasample-m-end.md)                                 | Beispielendzeit.                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | Startzeit des Mediums.                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | Medienstoppzeit.                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | Zeiger auf den Medientyp, wenn sich der Typ im Vergleich zum vorherigen Beispiel im Datenstrom geändert hat. |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | Streambezeichner.                                                                              |
| Öffentliche Membervariablen                                              | BESCHREIBUNG                                                                                     |
| [**m \_ cRef**](cmediasample-m-cref.md)                               | Verweisanzahl.                                                                                |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Konstruktormethode.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Destruktormethode. Virtuellen.                                                                     |
| [**SetPointer**](cmediasample-setpointer.md)                        | Legt den Zeiger auf den Speicherpuffer fest.                                                          |
| IMediaSample-Methoden                                                 | BESCHREIBUNG                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | Ruft einen Lese-/Schreibzeiger auf den Puffer ab.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Ruft die Größe des Puffers ab.                                                               |
| [**Gettime**](cmediasample-gettime.md)                              | Ruft die Streamzeiten ab, zu denen dieses Beispiel beginnen und abgeschlossen werden soll.                        |
| [**Settime**](cmediasample-settime.md)                              | Legt die Streamzeiten fest, zu denen dieses Beispiel gestartet und beendet werden soll.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Bestimmt, ob der Anfang des Beispiels ein Synchronisierungspunkt ist.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Gibt an, ob der Anfang dieses Beispiels ein Synchronisierungspunkt ist.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Bestimmt, ob es sich bei diesem Beispiel um ein Preroll-Beispiel handelt.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Gibt an, ob es sich bei diesem Beispiel um ein Preroll-Beispiel handelt.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Ruft die Länge der gültigen Daten im Puffer ab.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Legt die Länge der gültigen Daten im Puffer fest.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Ruft den Medientyp ab, wenn sich der Medientyp vom vorherigen Beispiel unterscheidet.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Legt den Medientyp für das Beispiel fest.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Ruft die Medienzeiten für dieses Beispiel ab.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Legt die Medienzeiten für dieses Beispiel fest.                                                           |
| IMediaSample2-Methoden                                                | BESCHREIBUNG                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Ruft die Eigenschaften des Beispiels ab.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Legt die Eigenschaften des Beispiels fest.                                                              |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




