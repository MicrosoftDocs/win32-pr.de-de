---
description: Bei der Verarbeitung einer Sicherung unter VSS haben Anfordernde und Writer zusammen ein stabiles Systemimage erstellt, aus dem Daten gesichert werden können. Dies erforderte koordination und die Erstellung einer Schattenkopie des aktuellen Systems.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Übersicht über die Verarbeitung einer Wiederherstellung unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b01094a02b823f372271f14c04801820407573b9351bfe7e2fc2ad9dc74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937958"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Übersicht über die Verarbeitung einer Wiederherstellung unter VSS

Bei der Verarbeitung einer Sicherung unter VSS haben Anfordernde und Writer zusammen ein stabiles Systemimage erstellt, aus dem Daten gesichert werden können. Dies erforderte koordination und die Erstellung einer Schattenkopie des aktuellen Systems.

Im Gegensatz zu einer VSS-Sicherung, bei der der Zweck der Koordination von Anfordernden und Writern darin besteht, ein stabiles Systemimage zu erstellen, aus dem Daten kopiert werden, besteht das Ziel einer VSS-basierten Wiederherstellung darin, Dateien auf den Datenträger zurück zu geben, die für Anwendungen (Writer), die derzeit auf dem System ausgeführt werden, am nützlichsten sind. Dies erfordert kein stabiles Systemimage, sodass keine Schattenkopie erforderlich ist.

Stattdessen liegt die Aufmerksamkeit auf der Vermeidung einer Unterbrechung der Writer-Aktivität, der Verhinderung der Erstellung inkonsistenter Datensätze auf dem Datenträger und der Möglichkeit, dass Writer daten bei Bedarf auswerten und zusammenführen können.

Wie bei einem Sicherungsvorgang erfordert eine VSS-Wiederherstellung sowohl Zugriff auf ein Sicherungskomponentendokument als auch auf Writermetadatendokumente. Diese Dokumente werden im Allgemeinen nicht durch Abfragen ausgeführter Anwendungen abgerufen, sondern aus Versionen, die als XML-Dokumente auf Sicherungsmedien gespeichert sind.

Wie bei Sicherungsvorgängen bleiben die Writer-Metadatendokumente schreibgeschützte Objekte, und (nach dem Abrufen) kann das Sicherungskomponentendokument weiterhin geändert werden. Änderungen des Sicherungskomponentendokuments ermöglichen Es Writern und Anfordernden, über Folgendes zu kommunizieren:

-   Überschreiben von [*Wiederherstellungsmethoden*](vssgloss-r.md) mit [*Wiederherstellungszielen*](vssgloss-r.md)
-   Verwenden [ *alternativer Standortzuordnungen*](vssgloss-a.md)
-   Wiederherstellen von Dateien an neuen Speicherorten auf dem Datenträger
-   Verwenden anderer Auswahlregeln als bei der Sicherung

Zur Vereinfachung der grundlegenden Tasks, die bei einer Wiederherstellung ablaufen, wurde dieser Überblick in die folgenden Themen unterteilt:

-   [Übersicht über die Wiederherstellungsin initialisierung](overview-of-restore-initialization.md)
-   [Übersicht über die Vorbereitung auf die Wiederherstellung](overview-of-preparing-for-restore.md)
-   [Übersicht über die tatsächliche Dateiwiederherstellung](overview-of-actual-file-restoration.md)
-   [Übersicht über die Bereinigung und Beendigung der Wiederherstellung](overview-of-restore-clean-up-and-termination.md)

 

 



