---
title: Strukturierte Storage Schnittstellen
description: Strukturierte Storage sind in drei Kategorien von Schnittstellen unterteilt.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Strukturierte Storage Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345c7b10ae4f73a80b3a263b9a9487c2172382b176404871b363aff336441a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661720"
---
# <a name="structured-storage-interfaces"></a>Strukturierte Storage Schnittstellen

Strukturierte Storage sind in drei Kategorien von Schnittstellen [unterteilt.](interfaces.md) Jede Menge stellt eine aufeinander folgende Deskriptions- oder Abstraktionsebene zwischen einer Verbunddatei, den in ihr enthaltenen Objekten und den physischen Medien dar, in denen diese einzelnen Komponenten gespeichert sind.

Die erste Kategorie von Schnittstellen besteht aus [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)und [**IRootStorage.**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) Die ersten beiden Schnittstellen definieren, wie Objekte in einer Verbunddatei gespeichert werden. Diese Schnittstellen bieten Methoden zum Öffnen von Speicherelementen, Committen und Rückgängig machen von Änderungen, Kopieren und Verschieben von Elementen sowie Lesen und Schreiben von Streams. Diese Schnittstellen erkennen die nativen Datenformate der einzelnen Objekte nicht und verfügen daher nicht über Methoden zum Speichern dieser Objekte im persistenten Speicher. Die **IRootStorage-Schnittstelle** verfügt über eine einzelne Methode zum Zuordnen eines Verbunddokuments zu einem zugrunde liegenden Dateisystemnamen. Clients müssen diese Schnittstellen für ihre Verbunddateien implementieren.

Die zweite Kategorie von Schnittstellen besteht aus den [**IPersist-Schnittstellen,**](/windows/win32/api/objidl/nn-objidl-ipersist) die Objekte implementieren, um ihre persistenten Daten zu verwalten. Diese Schnittstellen stellen Methoden zum Lesen der Datenformate einzelner Objekte bereit und wissen daher, wie sie gespeichert werden. Objekte sind für die Implementierung dieser Schnittstellen verantwortlich, da Clients die nativen Datenformate ihrer geschachtelten Objekte nicht kennen. Diese Schnittstellen verfügen jedoch nicht über Informationen zu bestimmten physischen Speichermedien.

Eine dritte Kategorie besteht aus einer einzelnen Schnittstelle, [**ILockBytes,**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)die Methoden zum Schreiben von Dateien auf bestimmte physische Medien wie eine Festplatte oder ein Bandlaufwerk bietet. Die meisten Anwendungen implementieren jedoch nicht die **ILockBytes-Schnittstelle,** da COM bereits Implementierungen für die beiden häufigsten Situationen bietet, bei denen es sich um dateibasierte Implementierung und speicherbasierte Implementierung handelt. Das Verbunddateispeicherobjekt ruft die **ILockBytes-Methoden** auf, die Sie nicht direkt in der Implementierung aufrufen.

## <a name="compound-file-implementation-limits"></a>Grenzwerte für die Implementierung von Verbunddatei

Die COM-Implementierung der Structured Storage-Architektur wird als *Verbunddateien bezeichnet.* Storage-Objekte, die in Verbunddateien implementiert sind, enthalten eine Implementierung der [**Schnittstellen IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und [**IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Zeiger auf die Verbunddateiimplementierung dieser Schnittstellen werden durch Aufrufen der [**StgCreateStorageEx-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) zum Erstellen eines neuen Verbunddateiobjekts oder [**stgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) zum Öffnen einer zuvor erstellten Verbunddatei erworben.

Eine alternative Methode zum Abrufen eines Zeigers auf die Verbunddateiimplementierung dieser Schnittstellen ist das Aufrufen der älteren und eingeschränkteren [**StgCreateDocfile-**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder [**StgOpenStorage-Funktion.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) Alle vier Funktionen werden als Verbunddateiimplementierungen behandelt.

Die Verbunddateiimplementierung kann für die Verwendung von 512- oder 4096-Byte-Sektoren konfiguriert werden, wie in der [**STGOPTIONS-Struktur**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) definiert.

Die Verbunddateiimplementierung von Verbunddateien unterliegt den folgenden Implementierungseinschränkungen.



| Begrenzung                                           | Verbunddatei                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateigrößenlimits:                               | 512: 2 Gigabyte (GB) 4096: Bis zu den Grenzwerten des Dateisystems<br/>                                                                                                                    |
| Maximale Heapgröße, die für geöffnete Elemente erforderlich ist:   | 512: 4 MEGABYTE (MB) 4096: Bis zu den Grenzwerten für virtuellen Arbeitsspeicher<br/>                                                                                                                 |
| Gleichzeitiger Stamm wird geöffnet (öffnet dieselbe Datei): | Wenn STGM \_ READ und STGM SHARE DENY WRITE angegeben werden, werden Grenzwerte durch die \_ \_ \_ Dateisystemgrenzwerte vorgegeben. Andernfalls gilt ein Grenzwert von 20 gleichzeitigen Root-Öffnen derselben Datei. |
| Anzahl der Elemente in einer Datei:                   | 512: Unbegrenzt, aber die Leistung kann beeinträchtigt werden, wenn elemente in den Tausenden von 4096 zahlen: Unbegrenzt<br/>                                                                         |



 

Aufgrund des Grenzwerts für die Heapgröße von 4 MB ist die Anzahl der offenen Elemente im transaktionsbasierten Modus in der Regel auf mehrere Tausend Elemente beschränkt.

 

