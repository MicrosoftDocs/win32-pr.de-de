---
title: Bandsicherung
description: Ein bandvolume besteht aus einem Aufzeichnungsmedium und seinem physischen Netzbetreiber. Jedes bandvolume verfügt über eine oder mehrere Partitionen. Partitionen werden in der Regel durch Datei Markierungen oder Setmarks in Abschnitte unterteilt. Es gibt drei Arten von Datei Markierungen.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- Sicherungs Sicherung, Band
- Sicherung der Bandsicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036504"
---
# <a name="tape-backup"></a>Bandsicherung

Ein *bandvolume* besteht aus einem Aufzeichnungsmedium und seinem physischen Netzbetreiber. Die gesamte Bandlänge in einem Volume ist nicht für die Aufzeichnung von Daten verfügbar. Kurze Abschnitte am Anfang und am Ende des Bands sind dafür reserviert, das Band an die Hubs im Netzbetreiber anzufügen. Die erste Position auf dem Band, an der Daten aufgezeichnet werden können, ist der als Mittelwert Ende *Marker*, und die letzte Position wird als *Mittelpunkt des Markers* bezeichnet.

Jedes bandvolume verfügt über eine oder mehrere Partitionen. Eine Partition ist ein Teil des Volumes mit ihren eigenen Anfangs-und Endpunkten, die sich nicht mit einem anderen Teil des Volumes überschneidet. Jede Partition verfügt über drei vordefinierte Positionen. Die erste Position in einer Partition, an der Sie Daten aufzeichnen können, wird als *Anfang-der-Partition-Markierung* bezeichnet, und die letzte Position wird als Partitions *Ende-Marker* bezeichnet. Der *Marker für die frühe Warnung* befindet sich unmittelbar vor dem Ende der Partitions Markierung. Die Position der frühen Warnung benachrichtigt Band Anwendungen, dass gepufferte Daten auf das Band übertragen werden, bevor der Marker für das Ende der Partition erreicht wird.

Der Bereich zwischen den Anfangs-und Endpunkten einer Partition wird in der Regel durch *Datei Markierungen* oder *Setmarks* in Abschnitte unterteilt. Datei Markierungen und setmarkierungen sind spezielle aufgezeichnete Elemente, die keine Benutzerdaten enthalten. die Partition wird einfach in kleinere Bereiche aufgeteilt, um ein Adress Schema bereitzustellen. Datei Markierungen und setmarkierungen dienen ähnlichen Zwecken, aber setmarkierungen ermöglichen eine schnellere Positionierung von Bandlaufwerken mit hoher Kapazität.

In der Regel werden von Band Geräten Datei Markierungen und setmarkierungen unterstützt. Durch die Unterstützung beider Optionen können die Banddaten formatiert werden, sodass die Daten von den Daten von verschiedenen Datenträgervolumes getrennt werden und die Daten von den einzelnen Dateien auf einem Datenträger Volume getrennt werden

Ein weiteres aufgenommenes Element, das Standorte auf dem Band bezeichnet, ist eine *Lösch Lücke*, ein Bereich mit gelöschtem Band oder ein Muster, das vom Gerät nicht als Markierung oder als Benutzerdaten erkannt wird.

Es gibt drei Arten von Datei Markierungen. Ein *kurzes Datei Zeichen* enthält eine kurze Lösch Lücke, die nur überschrieben werden kann, wenn der Schreibvorgang vom Anfang der Partition oder von einem früheren langen Datei Zeichen ausgeführt wird. Eine *lange Datei Markierung* enthält eine lange Lösch Lücke, die es einer Anwendung ermöglicht, das Band am Anfang der Datei Markierung zu positionieren und das Datei Markierung und die Lösch Lücke zu überschreiben. Ein *normales Datei Zeichen* enthält keine Lösch Lücke. Bandgeräte, die Datei Markierungen verwenden, unterstützen entweder kurze und lange Datei Markierungen oder normale Datei Markierungen, aber nicht alle drei.

Der Bereich auf einer Partition zwischen Setmarks oder Filemarks ist für das Aufzeichnen von Daten verfügbar. Eine Einheit von Daten, die in ein Band geschrieben oder daraus gelesen wird, wird als Block bezeichnet.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Band Initialisierung](tape-initialization.md)
-   [Band Eingabe und-Ausgabe](tape-input-and-output.md)
-   [Erstellen einer Sicherungs Anwendung](creating-a-backup-application.md)
-   [Sichern und Wiederherstellen von Hardlinks](backing-up-and-restoring-hard-links.md)

 

 




