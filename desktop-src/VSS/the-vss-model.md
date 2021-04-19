---
description: VSS dient der Behebung der Probleme, die unter Häufige Probleme mit der Volumesicherung beschrieben werden.
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: Das VSS-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360046"
---
# <a name="the-vss-model"></a>Das VSS-Modell

VSS dient der Behebung der Probleme, die unter Häufige Probleme mit der [Volumesicherung](common-volume-backup-issues.md)beschrieben werden.

Das VSS-Modell umfasst Folgendes:

-   Der schattenkopiemechanismus. VSS bietet eine schnelle volumeerfassung des Zustands eines Datenträgers zu einem Zeitpunkt – eine [*Schatten Kopie*](vssgloss-s.md) des Volumes. Diese Volumekopie ist parallel zum Live Volume vorhanden und enthält Kopien aller Dateien auf dem Datenträger, die effektiv gespeichert und als separates Gerät verfügbar sind.
-   Einheitlicher Datei Zustand über Anwendungs Koordination. VSS bietet einen com-basierten, ereignisgesteuerten Prozess für prozessübergreifende Kommunikation, mit dem teilnehmende Prozesse den Systemstatus in Bezug auf Sicherungs-, Wiederherstellungs-und schattenkopievorgänge (volumeerfassung) bestimmen können. Diese Ereignisse definieren Phasen, nach denen Anwendungen, die Daten auf einem Datenträger ([*Writer*](vssgloss-w.md)) ändern, alle Ihre Dateien vor der Erstellung der Schatten Kopie in einen konsistenten Zustand bringen können.
-   Minimierung der Ausfallzeiten von Anwendungen. Die VSS-Schatten Kopie ist parallel mit einer Live Kopie des zu sichernden Volumes vorhanden. mit Ausnahme der kurzen Zeitspanne der Vorbereitung und Erstellung des Schatten Kopierens kann eine Anwendung ihre Arbeit fortsetzen. Die Zeit, die erforderlich ist, um eine Schatten Kopie zu erstellen, die zwischen [*Freeze*](vssgloss-f.md) -und [*Thaw*](vssgloss-t.md) -Ereignissen auftritt, dauert in der Regel ungefähr eine Minute.

    Während der Vorbereitung eines Writers auf eine Schatten Kopie, einschließlich leeren von e/a-Vorgängen und Speichern von Zuständen (siehe [Übersicht über Aufgaben vor der Sicherung](overview-of-pre-backup-tasks.md)), ist möglicherweise nicht trivial, Sie ist deutlich kürzer als die Zeit, die für die eigentliche Sicherung eines Volumes erforderlich ist – für große Volumes kann es mehrere Stunden dauern.

-   Vereinheitlichte Schnittstelle zu VSS. VSS abstrahiert die schattenkopiemechanismen innerhalb einer gemeinsamen Oberfläche und ermöglicht einem Hardwarehersteller das Hinzufügen und Verwalten der eindeutigen Features seiner eigenen Anbieter. Alle Sicherungs Anwendungen ([*Anforderer*](vssgloss-r.md)) und alle Writer sollten in der Lage sein, auf jedem Datenträger-Speichersystem auszuführen, das die VSS-Schnittstelle unterstützt.
-   Multivolumesicherung. VSS unterstützt [*schattenkopiesätze*](vssgloss-s.md), bei denen es sich um Sammlungen von Schatten Kopien handelt, über mehrere Arten von Datenträgervolumes von mehreren Anbietern Alle Schatten Kopien in einem Schattenkopiesatz werden mit dem gleichen Zeitstempel erstellt und weisen für einen Datenträger Status mit mehreren Datenträgern denselben Datenträger Status auf.
-   Unterstützung für Native Schatten Kopien. Ab Windows XP ist die Unterstützung von Schatten Kopien über VSS als System eigener Teil des Windows-Betriebssystems verfügbar. Solange mindestens ein NTFS-Datenträger auf einem System vorhanden ist, können diese Systeme so konfiguriert werden, dass Schatten Kopien aller auf Ihnen bereitgestellten Festplattensysteme unterstützt werden.

 

 



