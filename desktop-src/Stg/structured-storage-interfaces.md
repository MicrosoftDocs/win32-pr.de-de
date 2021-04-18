---
title: Strukturierte Speicher Schnittstellen
description: Strukturierte Speicherdienste sind in drei Kategorien von Schnittstellen organisiert.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Strukturierte Speicher Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0010a0d4dec4908111c8a5bb939f795f0a2b2eb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339499"
---
# <a name="structured-storage-interfaces"></a>Strukturierte Speicher Schnittstellen

Strukturierte Speicherdienste sind in drei Kategorien von [Schnittstellen](interfaces.md)organisiert. Jede Gruppe stellt einen aufeinander folgenden Grad der Dereferenzierung oder Abstraktion zwischen einer Verbund Datei, den darin enthaltenen Objekten und den physischen Medien dar, auf denen diese einzelnen Komponenten gespeichert werden.

Die erste Kategorie der Schnittstellen besteht aus [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)und [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). Die ersten beiden Schnittstellen definieren, wie Objekte in einer Verbund Datei gespeichert werden. Diese Schnittstellen stellen Methoden zum Öffnen von Speicherelementen, zum Commit und zum Zurücksetzen von Änderungen, zum Kopieren und Verschieben von Elementen sowie zum Lesen und Schreiben von Streams bereit. Diese Schnittstellen erkennen nicht die systemeigenen Datenformate der einzelnen Objekte und verfügen daher über keine Methoden zum Speichern dieser Objekte in einem persistenten Speicher. Die **irootstorage** -Schnittstelle verfügt über eine einzelne Methode zum Zuordnen eines Verbund Dokuments zu einem zugrunde liegenden Dateisystem Namen. Clients müssen diese Schnittstellen für Ihre Verbund Dateien implementieren.

Die zweite Kategorie von Schnittstellen besteht aus den [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist) -Schnittstellen, die von Objekten implementiert werden, um die persistenten Daten zu verwalten. Diese Schnittstellen stellen Methoden zum Lesen der Datenformate einzelner Objekte bereit und wissen daher, wie Sie gespeichert werden. -Objekte sind für die Implementierung dieser Schnittstellen verantwortlich, da Clients die systemeigenen Datenformate ihrer in der Liste eingefügten Objekte nicht kennen. Diese Schnittstellen haben jedoch keine Kenntnis von bestimmten physischen Speichermedien.

Eine dritte Kategorie besteht aus einer einzelnen Schnittstelle, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), die Methoden zum Schreiben von Dateien auf bestimmte physische Medien, wie z. b. eine Festplatte oder ein Bandlaufwerk, bereitstellt. Die meisten Anwendungen implementieren jedoch die **ILockBytes** -Schnittstelle nicht, da com bereits Implementierungen für die beiden häufigsten Situationen bereitstellt, bei denen es sich um eine dateibasierte Implementierung und eine speicherbasierte Implementierung handelt. Das Verbund Dateispeicher-Objekt ruft die **ILockBytes** -Methoden auf, die Sie nicht direkt in der-Implementierung aufrufen.

## <a name="compound-file-implementation-limits"></a>Implementierungs Limits für Verbund Dateien

Die com-Implementierung der strukturierten Speicherarchitektur wird als *Verbund Dateien* bezeichnet. Speicher Objekte, wie in Verbund Dateien implementiert, enthalten eine Implementierung der Schnittstellen [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

Zeiger auf die Implementierung dieser Schnittstellen in Verbund Dateien werden durch Aufrufen der [**stgcreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) -Funktion zum Erstellen eines neuen Verbund Datei Objekts oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) zum Öffnen einer zuvor erstellten Verbund Datei abgerufen.

Eine alternative Methode zum Abrufen eines Zeigers auf die Implementierung dieser Schnittstellen für die Verbund Datei ist das Aufrufen der älteren und eingeschränkteren [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) -oder [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) -Funktion. Alle vier Funktionen werden als Implementierungen von Verbund Dateien behandelt.

Die Implementierung der Verbund Datei kann so konfiguriert werden, dass Sie 512-oder 4096-Byte-Sektoren verwendet, wie in der [**stgoptions**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) -Struktur definiert.

Die Verbund Datei Implementierung von Verbund Dateien unterliegt den folgenden Implementierungs Einschränkungen.



| Begrenzung                                           | Verbund Datei                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateigrößen Limits:                               | 512:2 Gigabyte (GB) 4096: bis zu Dateisystem Limits<br/>                                                                                                                    |
| Maximale Heap Größe, die für geöffnete Elemente erforderlich ist:   | 512:4 Megabyte (MB) 4096: Grenzwerte für den virtuellen Arbeitsspeicher<br/>                                                                                                                 |
| Gleichzeitiges root wird geöffnet (öffnet dieselbe Datei): | Wenn "STGM \_ Read" und "STGM \_ Freigabe \_ Deny Write" \_ festgelegt sind, werden die Limits durch die Dateisystem Limits vorgegeben. Andernfalls gibt es eine Beschränkung von 20 gleichzeitigen Stamm Öffne der gleichen Datei. |
| Anzahl von Elementen in einer Datei:                   | 512: unbegrenzt, aber die Leistung kann beeinträchtigt werden, wenn die Anzahl der Elemente in der Tausender 4096: unbegrenzt liegt.<br/>                                                                         |



 

Aufgrund der 4-MB-Heap Größenbeschränkung ist die Anzahl offener Elemente im transaktiven Modus in der Regel auf mehrere tausend Elemente beschränkt.

 

