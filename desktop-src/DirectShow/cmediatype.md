---
description: Die CMediaType-Klasse verwaltet Medientypen. Diese Klasse erbt die AM \_ MEDIA \_ TYPE-Struktur. Sie kann in eine Variable vom Typ AM \_ MEDIA TYPE um \_ werden.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: CMediaType-Klasse (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49680848fc764cdbbdfeaf3bea363f29427a745297ef4fb39bca09159aa582f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831945"
---
# <a name="cmediatype-class"></a>CMediaType-Klasse

![cmediatype-Klassenhierarchie](images/mtype01.png)

Die `CMediaType` -Klasse verwaltet Medientypen. Diese Klasse erbt die [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Sie kann in eine Variable vom Typ **AM \_ MEDIA TYPE (AM MEDIA \_ TYPE) typt werden.**



| Öffentliche Methoden                                                      | BESCHREIBUNG                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Konstruktormethode.                                                            |
| [**~CMediaType**](cmediatype--cmediatype.md)                       | Destruktormethode.                                                             |
| [**Festgelegt**](cmediatype-set.md)                                       | Legt den Medientyp von einem anderen Medientyp fest.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Bestimmt, ob diesem Objekt ein Haupttyp zugewiesen wurde.              |
| [**type**](cmediatype-type.md)                                     | Ruft den Haupttyp ab.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Gibt den Haupttyp an.                                                      |
| [**Untertyp**](cmediatype-subtype.md)                               | Ruft den Untertyp ab.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Gibt den Untertyp an.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Bestimmt, ob die Beispiele eine feste Größe oder eine variable Größe haben.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Bestimmt, ob der Stream temporale Komprimierung verwendet.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Ruft die Stichprobengröße ab.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Gibt eine feste Stichprobengröße an oder gibt an, dass Stichproben eine variable Größe haben. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Gibt an, dass Beispiele keine feste Größe haben.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Gibt an, ob Beispiele mithilfe der temporalen Komprimierung komprimiert werden.           |
| [**Format**](cmediatype-format.md)                                 | Ruft einen Zeiger auf den Formatblock ab.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Ruft die Länge des Formatblocks ab.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Gibt den Formattyp an                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Ruft den Formattyp ab.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Gibt den Formatblock an.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Löscht den Formatblock.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Weist Arbeitsspeicher für den Formatblock zu.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Gibt den Formatblock einer neuen Größe neu zu.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Initialisiert den Medientyp.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Bestimmt, ob dieser Medientyp einem teilweise angegebenen Medientyp entspricht.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Bestimmt, ob der Medientyp teilweise definiert ist.                             |
| Operatoren                                                           | Beschreibung                                                                    |
| [**operator =**](cmediatype-operator-.md)                          | Überladen den Zuweisungsoperator zum Kopieren eines Medientyps.                        |
| [**operator ==**](cmediatype-operator--.md)                        | Prüft auf Gleichheit zwischen `CMediaType`-Objekten.                               |
| [**operator !=**](cmediatype-operator-neq.md)                      | Prüft auf Ungleichheit zwischen `CMediaType`-Objekten.                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




