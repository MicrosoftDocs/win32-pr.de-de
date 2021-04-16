---
title: Layout von IMAPI-Multisession
description: IMAPI bietet Anwendungsentwicklern die Möglichkeit, ISO 9660-und UDF-Dateisystem Images zu erstellen und Sie auf CD, DVD und Blu-Ray \ 8482; zu brennen. optische Medien.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104556844"
---
# <a name="imapi-multisession-layout"></a>Layout von IMAPI-Multisession

IMAPI bietet Anwendungsentwicklern die Möglichkeit, ISO 9660-und UDF-Dateisystem Images zu erstellen und Sie auf CD-, DVD-und Blu-Ray-™ optischen Medien zu brennen. Mit Windows 7 bietet IMAPI zusätzliche Unterstützung für das Brennen von mehreren Sitzungen auf DVD-und Blu-Ray-™ erneut beschreibbare Medien.

In der folgenden Dokumentation wird das Festplattenlayout erläutert, das von IMAPI zum Implementieren von mehreren Sitzungen verwendet wird. Diese Informationen sollten verwendet werden, um die Interoperabilität zwischen IMAPI und anderer brennender Software zu gewährleisten und Entwicklern dieser Software das Erstellen von IMAPI-kompatiblen Festplatten Abbildern mit mehreren Sitzungen zu ermöglichen.

> [!Note]  
> Ein Beispiel für die Erstellung einer mehr sitzenden CD finden Sie unter [Erstellen eines mehrteiligen](creating-a-multisession-disc.md)Festplatten Datenträgers.

 

## <a name="multisession-on-sequential-media"></a>Multisession auf sequenziellen Medien

Die IMAPI-Implementierung von Multisession auf sequenziellen Medien wird für die Verwendung mit CD-r, CD-RW, DVD-r, DVD + R und Blu-Ray™ Medien unterstützt. IMAPI verwendet den Session-at-Once-Aufzeichnungsmodus für CD-RW. Folglich wird das Format in diesem Szenario als sequenzieller Medientyp betrachtet.

In einem Szenario, in dem mehrere Sitzungen auf sequenziellen Medien mithilfe der benutzerdefinierten Funktion verwendet werden, schreibt IMAPI die Anker Strukturen (UDF-Anker Volume Deskriptor Zeiger-avdp), volumestrukturen (UDF-volumedeskriptorsequenz-VDS) und die Dateisystem-Metadatenstrukturen (UDF-Datei Satz Deskriptor-FSD) zu Beginn jeder neuen

![Diagramm, das die Dateisystem-Metadatenstruktur mit dem ' Import/F S-Bereitstellungs Punkt ' anzeigt, wird mit einem roten Pfeil an der ' Anker ' der physischen Sitzung 2 angezeigt.](images/multises1.png)

> [!Note]  
> In dieser Abbildung wird das IMAPI-Festplattenlayout bei Verwendung von UDF 2,50 mit redundanten Metadaten veranschaulicht.

 

Die auf sequenziell aufgezeichneten Medien gespeicherten Daten bestehen aus einer Reihe physischer Sitzungen. Jede Sitzung enthält ein ganzes Dateisystem, das Benutzerdaten als eine Gruppe von Dateien darstellt, die in Verzeichnissen organisiert sind. Die Metadaten des Dateisystems bestehen aus einer Reihe von hierarchisch organisierten Datenstrukturen. Am Anfang der Hierarchie befinden sich Anker Strukturen (avdp), die sich unter vordefinierte logische Block Adressen (LBAs) befinden. Die Anker Strukturen geben die Speicherorte der nächsten Ebenen Strukturen an, die nicht über vordefinierte Adressen verfügen. Die nächste Hierarchieebene nach Anker Strukturen enthält die volumestrukturen (VDS), die die Eigenschaften des Volumes beschreiben und auf die Dateisystem-Metadatenstrukturen (FSD) verweisen, die wiederum einzelne Dateien und Verzeichnisse beschreiben.

## <a name="multisession-on-rewritable-media"></a>Mehrfach Sitzung auf neu beschreibbaren Medien

Der Ansatz für sequenzielle Medien, die im vorherigen Abschnitt beschrieben wurden, ist nicht kompatibel mit dem wieder beschreibbaren (nicht sequenziellen) Medium. Zu diesen Medienformaten zählen DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ reschreibbar und andere zufällige beschreibbare Medien, wie z. b. Iomega REV Disks. Ein erneut beschreibbares Medium unterstützt nicht das Konzept physischer Sitzungen, die logischen Sitzungen entsprechen, bei denen es sich um einzelne Inkremente handelt, die durch eine Mastering-Anwendung zugesichert werden. Es wird nur eine einzelne physische Sitzung verfügbar gemacht. dabei handelt es sich um einen Bereich, der am Anfang der Festplatte steht, der den gesamten adressierbaren Bereich darstellt, in dem mehrere logische Sitzungen enthalten sein können.

> [!Note]  
> Obwohl es sich bei DVD-RW um eine Ausnahme handelt, da Sie das Konzept einer physischen Sitzung im sequenziellen Modus unterstützt, wird diese Funktion derzeit von IMAPI nicht unterstützt.

 

Um dem Mangel an einer eins-zu-Eins-Zuordnung zwischen physischen und logischen Sitzungen in neu beschreibbaren Formaten zu begegnen, aktualisiert IMAPI die Anker Strukturen (avdp) in der *ersten* logischen Sitzung selektiv, sodass Sie am Anfang der *letzten* logischen Sitzung auf die neuen volumestrukturen (VDS) und Dateisystem-Metadatenstrukturen (FSD) verweisen, wie im folgenden Diagramm dargestellt:

![Diagramm, das die Dateisystem-Metadatenstruktur mit dem ' Import/F S-Bereitstellungs Punkt ' anzeigt, wird mit einem roten Pfeil an der ' Anker ' der logischen Sitzung 1 angegeben.](images/multises2.png)

> [!Note]  
> In dieser Abbildung wird das IMAPI-Festplattenlayout bei Verwendung von UDF 2,50 mit redundanten Metadaten veranschaulicht.

 

Beim Hinzufügen einer neuen logischen Sitzung zu einer wieder Schreib baren Diskette bestimmt IMAPI zuerst das Ende der letzten logischen Sitzung durch Analysieren der Volumemetadaten (VDS). IMAPI fügt dann die neue logische Sitzung mit dem neuen Anker (avdp), dem Volume (VDS) und den Dateisystem-Metadatenstrukturen (FSD) hinzu, die physisch mit der zuvor aufgezeichneten logischen Sitzung zusammenhängend sind. Der letzte Schritt erfordert, dass die Anker Strukturen (avdp) am Anfang der ersten logischen Sitzung aktualisiert werden, um auf die volumestrukturen (VDS) in der *neuen* logischen Sitzung zu verweisen. Das operative Ergebnis ist mit dem sequenziellen Medium identisch.

## <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

-   **Partitions Layout**

    Um IMAPI-Kompatibilität zu erzielen, wird empfohlen, dass Entwickler von Drittanbietern die in dieser Dokumentation beschriebenen Festplatten Layouts verwenden. Entwickler sollten Layouts mit Dateisystem Partitionen vermeiden, die den gesamten Datenträger belegen, da dies das Aufzeichnen von Anwendungen erfordert, um den freien Speicherplatz in vorhandenen Partitionen zu ermitteln, wenn Daten an die Festplatte angefügt werden müssen. Oft erreichen die Aufzeichnungs Anwendungen dies, indem Sie proprietäre Marker auf der Festplatte verwenden, um anzugeben, wie viel Speicherplatz tatsächlich von Benutzerdaten belegt wird. Solche Festplatten Layouts sind mit IMAPI nicht kompatibel, da die proprietären Marker außerhalb der Anwendung, für die Sie erstellt wurden, nicht erkannt werden.

-   **UDF-Partitionstyp**

    IMAPI verwendet den schreibgeschützten UDF-Partitionstyp **in der Implementierung** von Multisession auf neu beschreibbaren Medien. Entwickler von Drittanbieter-Brennsoftware sollten den schreibgeschützten UDF-Partitionstyp verwenden, um Kompatibilität mit Windows **-vorschautem** brennen über IMAPI zu erzielen. Wenn ein anderer UDF-Partitionstyp verwendet wird, z. b. " **Rewrite Table** ", kann IMAPI keine Unterstützung für die

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Multi-Session-CD](creating-a-multisession-disc.md)
</dt> <dt>

[**Imultisessionrandomwrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




