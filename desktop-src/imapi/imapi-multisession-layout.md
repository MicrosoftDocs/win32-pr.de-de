---
title: IMAPI-Multisessionlayout
description: IMAPI bietet Anwendungsentwicklern die Möglichkeit, ISO 9660- und UDF-Dateisystemimages zu erstellen und auf CD, DVD und Blu-Ray \ 8482 zu speichern. optische Medien.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d816d293a3474f46dc3a48577a46615672103099dc2aa561d393953f29ccf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249411"
---
# <a name="imapi-multisession-layout"></a>IMAPI-Multisessionlayout

IMAPI bietet Anwendungsentwicklern die Möglichkeit, ISO 9660- und UDF-Dateisystemimages zu erstellen und auf cd-, DVD- und Blu-Ray™ optischen Medien zu speichern. Mit Windows 7 bietet IMAPI zusätzliche Unterstützung für Multisessions auf DVD und Blu-Ray™ umschreibbaren Medien.

In der folgenden Dokumentation wird das Datenträgerlayout ausführlich beschrieben, das die IMAPI zum Implementieren von Multisession verwendet. Diese Informationen sollten verwendet werden, um die Interoperabilität zwischen IMAPI und anderer softwarekompatibeler Software sicherzustellen und den Entwicklern dieser Software das Erstellen VON IMAPI-kompatiblen Multisession-Datenträgerimages zu ermöglichen.

> [!Note]  
> Ein Beispiel für die Erstellung eines Multisession-Datenträgers finden Sie unter [Erstellen eines Multisession-Datenträgers.](creating-a-multisession-disc.md)

 

## <a name="multisession-on-sequential-media"></a>Multisession auf sequenziellen Medien

Die IMAPI-Implementierung von Multisession auf sequenziellen Medien wird für die Verwendung mit CD-R-, CD-RW-, DVD-R-, DVD+R- und Blu-Ray™medien unterstützt. IMAPI verwendet den Session-At-Once-Aufzeichnungsmodus für CD-RW. Daher wird das Format in diesem Szenario als sequenzieller Medientyp betrachtet.

In einem Szenario mit Multisession auf sequenziellen Medien mithilfe von UDF schreibt IMAPI die Ankerstrukturen (UDF Anchor Volume Descriptor Pointer - AVDP), Volumestrukturen (UDF Volume Descriptor Sequence - VDS) und die Dateisystemmetadatenstrukturen (UDF File Set Descriptor - FSD) zu Beginn jeder neuen Sitzung, wie im folgenden Diagramm dargestellt:

![Diagramm, das die Dateisystemmetadatenstruktur mit dem "Import/F S-Einbindungspunkt" mit einem roten Pfeil am "Anker" der physischen Sitzung 2 zeigt.](images/multises1.png)

> [!Note]  
> Diese Abbildung veranschaulicht das IMAPI-Datenträgerlayout bei Verwendung von UDF 2.50 mit redundanten Metadaten.

 

Die auf sequenziell aufgezeichneten Medien gespeicherten Daten bestehen aus einer Reihe von physischen Sitzungen. Jede Sitzung enthält ein vollständiges Dateisystem, das Benutzerdaten als eine Reihe von Dateien darstellt, die in Verzeichnissen organisiert sind. Die Dateisystemmetadaten bestehen aus einer Reihe von hierarchisch organisierten Datenstrukturen. Am oberen Rand der Hierarchie befinden sich Ankerstrukturen (AVDP), die sich unter vordefinierten logischen Blockadressen (Logical Block Addresses, LBAs) befinden. Die Ankerstrukturen geben die Positionen der Strukturen der nächsten Ebene an, die keine vordefinierten Adressen haben. Die nächste Hierarchieebene nach Ankerstrukturen enthält die Volumestrukturen (VDS), die die Eigenschaften des Volumes beschreiben und auf die Dateisystemmetadatenstrukturen (File System Metadata Structures, FSD) verweisen, die wiederum einzelne Dateien und Verzeichnisse beschreiben.

## <a name="multisession-on-rewritable-media"></a>Multisession auf rewritable Media

Der im vorherigen Abschnitt beschriebene Ansatz für sequenzielle Medien ist nicht mit rewritablen (nicht sequenziellen) Medien kompatibel. Zu diesen Medienformaten gehören DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable und andere zufällig beschreibbare Medien wie Iomaga REV-Datenträger. Umschreibbare Medien unterstützen nicht das Konzept physischer Sitzungen, die logischen Sitzungen entsprechen. Dabei handelt es sich um einzelne Inkremente, die von einer Masteranwendung ausgeführt werden. Es wird nur eine einzelne physische Sitzung verfügbar gemacht. Dabei handelt es sich um einen Bereich, der am Anfang des Datenträgers beginnt und den gesamten adressierbaren Bereich darstellt, der mehrere logische Sitzungen enthalten kann.

> [!Note]  
> DVD-RW ist zwar eine Ausnahme, da es das Konzept einer physischen Sitzung im sequenziellen Modus unterstützt, diese Funktion wird von IMAPI derzeit jedoch nicht unterstützt.

 

Um das Fehlen einer 1:1-Zuordnung zwischen physischen und logischen Sitzungen in umschreibbaren Formaten zu beheben, aktualisiert IMAPI selektiv die Ankerstrukturen (AVDP) in der *ersten* logischen Sitzung, um auf die neuen Volumestrukturen (VDS) und Dateisystemmetadatenstrukturen (File System Metadata Structures, FSD) am Anfang der *letzten* logischen Sitzung zu verweisen, wie im folgenden Diagramm dargestellt:

![Diagramm, das die Dateisystemmetadatenstruktur mit dem "Import/F S-Einbindungspunkt" mit einem roten Pfeil am "Anker" der logischen Sitzung 1 zeigt.](images/multises2.png)

> [!Note]  
> Diese Abbildung veranschaulicht das IMAPI-Datenträgerlayout bei Verwendung von UDF 2.50 mit redundanten Metadaten.

 

Beim Hinzufügen einer neuen logischen Sitzung zu einem erneut beschreibbaren Datenträger bestimmt die IMAPI zunächst das Ende der letzten logischen Sitzung, indem die Volumemetadaten (VDS) analysiert werden. IMAPI fügt dann die neue logische Sitzung hinzu, die mit dem neuen Anker (AVDP), dem Volume (VDS) und den Dateisystemmetadatenstrukturen (File System Metadata Structures, FSD) abgeschlossen ist und physisch mit der zuvor aufgezeichneten logischen Sitzung verbunden ist. Der letzte Schritt erfordert, dass die Ankerstrukturen (AVDP) zu Beginn der ersten logischen Sitzung aktualisiert werden, um auf die Volumestrukturen (VDS) in der *neuen* logischen Sitzung zu verweisen. Das Betriebsergebnis ist dasselbe wie bei sequenziellen Medien.

## <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

-   **Partitionslayout**

    Um IMAPI-Kompatibilität zu erreichen, wird empfohlen, dass Softwareentwickler von Drittanbietern die in dieser Dokumentation beschriebenen Datenträgerlayouts verwenden. Entwickler sollten Layouts mit Dateisystempartitionen vermeiden, die den gesamten Datenträger belegen, da dies erfordert, dass Aufzeichnungsanwendungen freien Speicherplatz in vorhandenen Partitionen finden, wenn Daten an den Datenträger angefügt werden müssen. Häufig erreichen die Aufzeichnungsanwendungen dies, indem proprietäre Marker auf dem Datenträger verwendet werden, um anzugeben, wie viel Speicherplatz tatsächlich von Benutzerdaten belegt wird. Solche Datenträgerlayouts sind mit IMAPI nicht kompatibel, da die proprietären Marker außerhalb der Anwendung, für die sie erstellt wurden, nicht erkannt werden.

-   **UDF-Partitionstyp**

    IMAPI verwendet den **Schreibgeschützten** UDF-Partitionstyp in der Implementierung von Multisession auf neu beschreibbaren Medien. Entwickler von Software von Drittanbietern sollten den **Schreibgeschützten** UDF-Partitionstyp verwenden, um Kompatibilität mit Windows mastered- über IMAPI zu erreichen. Wenn ein anderer UDF-Partitionstyp wie **Rewritable** verwendet wird, kann IMAPI keine Masterunterstützung bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Multisession-Datenträgers](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




