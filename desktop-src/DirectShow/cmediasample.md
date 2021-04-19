---
description: Die cmediasample-Klasse definiert ein Medien Beispiel, das die IMediaSample2-Schnittstelle unterstützt. Das Medien Beispiel enthält einen Zeiger auf einen Speicherpuffer und verschiedene Eigenschaften, die als geschützte Element Variablen gespeichert sind.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Cmediasample-Klasse (amfilter. h)
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
ms.openlocfilehash: 72cfe0f86ff6b6643f2f7793822899136a5c6454
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358192"
---
# <a name="cmediasample-class"></a>Cmediasample-Klasse

![cmediasample-Klassenhierarchie](images/wutil03.png)

Die- `CMediaSample` Klasse definiert ein Medien Beispiel, das die [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle unterstützt. Das Medien Beispiel enthält einen Zeiger auf einen Speicherpuffer und verschiedene Eigenschaften, die als geschützte Element Variablen gespeichert sind.

Medien Beispiele werden von Zuordnungen erstellt, die von der [**cbasezucator**](cbaseallocator.md) -Klasse abgeleitet werden. Der- `CMediaSample` Konstruktor erhält einen Zeiger auf einen zugeordneten Puffer sowie die Größe des Puffers. Andere Eigenschaften werden in der Regel mithilfe von [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstellen Methoden festgelegt und abgerufen.

Der Lebenszyklus eines Medien Beispiels unterscheidet sich von dem der meisten COM-Objekte:

-   Die Zuweisung enthält eine Liste mit kostenlosen Beispielen. Wenn ein Filter ein neues Beispiel benötigt, ruft er die [**imemzuordcator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode des zuorders auf. Die Zuweisung Ruft eine Stichprobe aus der kostenlosen Liste ab, erhöht den Verweis Zähler der Stichprobe und gibt einen Zeiger auf das Beispiel zurück.
-   Nachdem der Filter mit dem Beispiel erstellt wurde, ruft er die **IUnknown:: Release** -Methode für das Beispiel auf. Im Gegensatz zu den meisten-Objekten wird das Beispiel nicht selbst gelöscht, wenn der Verweis Zähler Null erreicht. Stattdessen wird die [**imemzucator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode für die Zuweisung aufgerufen, und die Zuweisung gibt das Beispiel an die freie Liste zurück.
-   Die Zuweisung zerstört keine Stichproben, bis die [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) -Methode aufgerufen wird.



| Geschützte Member-Variablen                                           | BESCHREIBUNG                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Beispieleigenschaftenflags.                                                                          |
| [**m \_ dwtypespecificflags**](cmediasample-m-dwtypespecificflags.md) | Typspezifische Flags.                                                                            |
| [**m \_ pbuffer**](cmediasample-m-pbuffer.md)                         | Zeiger auf den Arbeitsspeicher Puffer, der die Mediendaten enthält.                                      |
| [**m \_ laktiv**](cmediasample-m-lactual.md)                         | Länge der gültigen Daten im Puffer in Bytes.                                               |
| [**m \_ cbbuffer**](cmediasample-m-cbbuffer.md)                       | Größe des Puffers in Bytes.                                                                   |
| [**m- \_ pallocator**](cmediasample-m-pallocator.md)                   | Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Zeiger auf das nächste Beispiel in der Liste der-Beispiele des Zuordners.                                  |
| [**m \_ Start**](cmediasample-m-start.md)                             | Die Startzeit für das Beispiel.                                                                              |
| [**m \_ Ende**](cmediasample-m-end.md)                                 | Beispiel Endzeit.                                                                                |
| [**m \_ mediastart**](cmediasample-m-mediastart.md)                   | Start Zeit des Mediums.                                                                               |
| [**m \_ mediaend**](cmediasample-m-mediaend.md)                       | Die Endzeit des Mediums.                                                                                |
| [**m \_ pmediatype**](cmediasample-m-pmediatype.md)                   | Ein Zeiger auf den Medientyp, wenn sich der Typ aus dem vorherigen Beispiel im Datenstrom geändert hat. |
| [**m \_ dwstreamid**](cmediasample-m-dwstreamid.md)                   | Datenstrom Bezeichner.                                                                              |
| Öffentliche Element Variablen                                              | BESCHREIBUNG                                                                                     |
| [**m- \_ kref**](cmediasample-m-cref.md)                               | Verweis Zähler.                                                                                |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                                     |
| [**Cmediasample**](cmediasample-cmediasample.md)                    | Konstruktormethode.                                                                             |
| [**~ Cmediasample**](cmediasample--cmediasample.md)                 | Dekonstruktormethode. Virtu.                                                                     |
| [**Setpointer**](cmediasample-setpointer.md)                        | Legt den Zeiger auf den Arbeitsspeicher Puffer fest.                                                          |
| Imediasample-Methoden                                                 | BESCHREIBUNG                                                                                     |
| [**Getpointer**](cmediasample-getpointer.md)                        | Ruft einen Lese-/schreibzeiger auf den Puffer ab.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Ruft die Größe des Puffers ab.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Ruft die streamzeiten ab, zu denen das Beispiel beginnen und fertigstellen soll.                        |
| [**SetTime**](cmediasample-settime.md)                              | Legt die streamzeiten fest, zu denen das Beispiel gestartet und beendet werden soll.                             |
| [**Issyncpoint**](cmediasample-issyncpoint.md)                      | Bestimmt, ob der Anfang des Beispiels ein Synchronisierungs Punkt ist.                           |
| [**Setsyncpoint**](cmediasample-setsyncpoint.md)                    | Gibt an, ob der Anfang dieses Beispiels ein Synchronisierungs Punkt ist.                      |
| [**Ispreroll**](cmediasample-ispreroll.md)                          | Bestimmt, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt.                                                  |
| [**Setpreroll**](cmediasample-setpreroll.md)                        | Gibt an, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt.                                              |
| [**Getactualdatalength**](cmediasample-getactualdatalength.md)      | Ruft die Länge der gültigen Daten im Puffer ab.                                           |
| [**Setactualdatalength**](cmediasample-setactualdatalength.md)      | Legt die Länge der gültigen Daten im Puffer fest.                                                |
| [**Getmediatype**](cmediasample-getmediatype.md)                    | Ruft den Medientyp ab, wenn der Medientyp vom vorherigen Beispiel abweicht.                   |
| [**Setmediatype**](cmediasample-setmediatype.md)                    | Legt den Medientyp für das Beispiel fest.                                                             |
| [**Isdiscontinuity**](cmediasample-isdiscontinuity.md)              | Bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.                                |
| [**Setdiscontinuity**](cmediasample-setdiscontinuity.md)            | Gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt.                            |
| [**Getmediatime**](cmediasample-getmediatime.md)                    | Ruft die Medien Zeiten für dieses Beispiel ab.                                                      |
| [**Setmediatime**](cmediasample-setmediatime.md)                    | Legt die Medien Zeiten für dieses Beispiel fest.                                                           |
| IMediaSample2-Methoden                                                | BESCHREIBUNG                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Ruft die Eigenschaften des Beispiels ab.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Legt die Eigenschaften des Beispiels fest.                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




