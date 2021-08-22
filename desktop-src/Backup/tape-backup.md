---
title: Bandsicherung
description: Ein Bandvolumen besteht aus einem Aufzeichnungsmedium und seinem physischen Netzbetreiber. Jedes Bandvolumen verfügt über eine oder mehrere Partitionen. Partitionen werden in der Regel durch Dateimarks oder Setmarks in Abschnitte unterteilt. Es gibt drei Arten von Dateimarks.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- Sicherungssicherung, Band
- Bandsicherungssicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217c1a536b8a1a345218d3748c6207e9b336b84eca4cea0f4e48b4e84c521733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588830"
---
# <a name="tape-backup"></a>Bandsicherung

Ein *Bandvolumen* besteht aus einem Aufzeichnungsmedium und seinem physischen Netzbetreiber. Die gesamte Bandlänge in einem Volume ist nicht für die Aufzeichnung von Daten verfügbar. Kurze Abschnitte am Anfang und Ende des Bandes sind für das Anfügen des Bandes an die Hubs im Netzbetreiber reserviert. Die erste Position auf dem Band, an der Daten aufgezeichnet werden können, ist der so genannte Anfang des mittleren Markers, und die letzte Position wird als *End-of-Medium-Marker bezeichnet.*

Jedes Bandvolumen verfügt über eine oder mehrere Partitionen. Eine Partition ist ein Teil des Volumes, der eigene Anfangs- und Endpunkte enthält, die sich nicht mit anderen Teilen des Volumes überschneiden. Jede Partition verfügt über drei vordefinierte Positionen. Die erste Position in einer Partition, an der Sie Daten aufzeichnen können, wird als Anfang *der* Partitionsmarkierung bezeichnet, und die letzte wird als *End-of-Partitionsmarker bezeichnet.* Der *Marker für frühzeitige Warnungen* befindet sich unmittelbar vor dem Marker für das Ende der Partition. Die Frühwarnposition benachrichtigt Bandanwendungen, gepufferte Daten auf das Band zu übertragen, bevor der Marker für das Ende der Partition erreicht wird.

Der Bereich zwischen dem Anfang und dem Endpunkt einer Partition wird in der Regel durch *Dateimarks* oder *Setmarks in Abschnitte unterteilt.* Dateimarks und Setmarks sind spezielle aufgezeichnete Elemente, die keine Benutzerdaten enthalten. Sie teilen die Partition einfach in kleinere Bereiche auf, um ein Adressschema zur Verfügung zu stellen. Dateimarks und Setmarks dienen ähnlichen Zwecken, aber Setmarks ermöglichen eine schnellere Positionierung auf Bandlaufwerken mit hoher Kapazität.

In der Regel unterstützen Bandgeräte Dateimarks und Setmarks. Durch die Unterstützung von beiden können Banddaten so formatiert werden, dass Durch Setmarks Daten von verschiedenen Datenträgervolumes und Dateimarks von einzelnen Dateien auf einem Datenträgervolume getrennt werden.

Ein weiteres aufgezeichnetes Element, das Positionen auf dem Band bezeichnet, ist eine Löschlücke, ein Bereich mit gelöschten Bändern oder ein Muster, das das Gerät nicht als Markierung oder als Benutzerdaten erkennt.

Es gibt drei Arten von Dateimarks. Ein *kurzes Dateizeichen* enthält eine kurze Löschlücke, die nur überschrieben werden kann, wenn der Schreibvorgang vom Anfang der Partition oder von einem früheren langen Dateimark ausgeführt wird. Ein *langes Dateizeichen* enthält eine lange Löschlücke, die es einer Anwendung ermöglicht, das Band am Anfang des Dateizeichens zu positionieren und die Dateimark- und Löschlücke zu überschreiben. Ein *normales Dateizeichen* enthält keine Löschlücke. Bandgeräte, die Dateimarks verwenden, unterstützen entweder kurze und lange Dateimarks oder normale Dateimarks, aber nicht alle drei.

Der Bereich auf einer Partition zwischen Setmarks oder Dateimarks ist zum Aufzeichnen von Daten verfügbar. Eine Dateneinheit, die auf ein Band geschrieben oder von diesem gelesen wird, wird als Block bezeichnet.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Bandin initialisierung](tape-initialization.md)
-   [Bandeingabe und -ausgabe](tape-input-and-output.md)
-   [Erstellen einer Sicherungsanwendung](creating-a-backup-application.md)
-   [Sichern und Wiederherstellen von hard-Links](backing-up-and-restoring-hard-links.md)

 

 




