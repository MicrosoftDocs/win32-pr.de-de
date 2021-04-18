---
description: Die cmediatype-Klasse verwaltet Medientypen. Diese Klasse erbt die am \_ \_ Medientyp-Struktur. Sie kann in eine Variable vom Typ "am Medientyp" umgewandelt werden \_ \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Cmediatype-Klasse (mtype. h)
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
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364930"
---
# <a name="cmediatype-class"></a>Cmediatype-Klasse

![cmediatype-Klassenhierarchie](images/mtype01.png)

Die- `CMediaType` Klasse verwaltet Medientypen. Diese Klasse erbt die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur. Sie kann in eine Variable vom Typ " **am \_ \_ Medientyp**" umgewandelt werden.



| Öffentliche Methoden                                                      | BESCHREIBUNG                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Cmediatype**](cmediatype-cmediatype.md)                         | Konstruktormethode.                                                            |
| [**~ Cmediatype**](cmediatype--cmediatype.md)                       | Dekonstruktormethode.                                                             |
| [**Set**](cmediatype-set.md)                                       | Legt den Medientyp von einem anderen Medientyp fest.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.              |
| [**type**](cmediatype-type.md)                                     | Ruft den Haupttyp ab.                                                      |
| [**Settype**](cmediatype-settype.md)                               | Gibt den Haupttyp an.                                                      |
| [**Untertyp**](cmediatype-subtype.md)                               | Ruft den Untertyp ab.                                                         |
| [**Setsubtype**](cmediatype-setsubtype.md)                         | Gibt den Untertyp an.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Bestimmt, ob die Stichproben eine festgelegte Größe oder eine Variable Größe aufweisen.                |
| [**Istemporalcompressed**](cmediatype-istemporalcompressed.md)     | Bestimmt, ob der Stream Temporale Komprimierung verwendet.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Ruft die Stichprobengröße ab.                                                     |
| [**Setsamplesize**](cmediatype-setsamplesize.md)                   | Gibt eine festgelegte Stichprobengröße an oder gibt an, dass Beispiele eine Variable Größe aufweisen. |
| [**Setvariablesize**](cmediatype-setvariablesize.md)               | Gibt an, dass die Stichproben keine festgelegte Größe aufweisen.                               |
| [**Settemporalcompression**](cmediatype-settemporalcompression.md) | Gibt an, ob Samples mithilfe der temporalen Komprimierung komprimiert werden.           |
| [**Ges**](cmediatype-format.md)                                 | Ruft einen Zeiger auf den Format Block ab.                                       |
| [**Formatlength**](cmediatype-formatlength.md)                     | Ruft die Länge des Format Blocks ab.                                      |
| [**Setformattype**](cmediatype-setformattype.md)                   | Gibt den Formattyp an                                                     |
| [**Format Type**](cmediatype-formattype.md)                         | Ruft den Formattyp ab.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Gibt den Format Block an.                                                    |
| [**Resetformatbuffer**](cmediatype-resetformatbuffer.md)           | Löscht den Format Block.                                                      |
| [**"Zuweisung"**](cmediatype-allocformatbuffer.md)           | Weist Speicher für den Format Block zu.                                         |
| [**Rezuweisung von formatbuffer**](cmediatype-reallocformatbuffer.md)       | Ordnet den Format Block neu einer neuen Größe zu.                                    |
| [**Initmediatype**](cmediatype-initmediatype.md)                   | Initialisiert den Medientyp.                                                    |
| [**Matchespartial**](cmediatype-matchespartial.md)                 | Bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.        |
| [**Ispartiallyspezifiziert**](cmediatype-ispartiallyspecified.md)     | Bestimmt, ob der Medientyp teilweise definiert ist.                             |
| Operatoren                                                           | Beschreibung                                                                    |
| [**Operator =**](cmediatype-operator-.md)                          | Über lädt den Zuweisungs Operator zum Kopieren eines Medientyps.                        |
| [**Operator = =**](cmediatype-operator--.md)                        | Prüft auf Gleichheit zwischen `CMediaType`-Objekten.                               |
| [**Operator! =**](cmediatype-operator-neq.md)                      | Prüft auf Ungleichheit zwischen `CMediaType`-Objekten.                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




