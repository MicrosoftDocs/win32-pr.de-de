---
description: Bei der Verarbeitung einer Sicherung unter VSS haben Anforderer und Writer zusammengearbeitet, um ein stabiles System Abbild zu erstellen, mit dem die Daten gesichert werden müssen, wofür eine Koordination und Erstellung einer Schatten Kopie des aktuellen Systems erforderlich war.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Übersicht über die Verarbeitung einer Wiederherstellung unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356908"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Übersicht über die Verarbeitung einer Wiederherstellung unter VSS

Bei der Verarbeitung einer Sicherung unter VSS haben Anforderer und Writer zusammengearbeitet, um ein stabiles System Abbild zu erstellen, mit dem die Daten gesichert werden müssen, wofür eine Koordination und Erstellung einer Schatten Kopie des aktuellen Systems erforderlich war.

Anders als bei einer VSS-Sicherung, bei der der Zweck der Koordination von Anforderer und Writer darin besteht, ein stabiles System Abbild zu erstellen, aus dem Daten kopiert werden sollen, besteht das Ziel einer VSS-basierten Wiederherstellung darin, Dateien auf eine Weise zurückzugeben, die für Anwendungen (Writer), die derzeit im System ausgeführt werden, am nützlichsten Dies erfordert kein stabiles System Abbild, sodass keine Schatten Kopie erforderlich ist.

Stattdessen konzentriert sich der Schwerpunkt auf die Vermeidung von Unterbrechungen der Schreiber Aktivität, verhindert das Erstellen inkonsistenter Datasets auf dem Datenträger und ermöglicht es den Writern, bei Bedarf Daten auszuwerten und zusammenzuführen.

Wie bei einem Sicherungs Vorgang ist für eine VSS-Wiederherstellung sowohl der Zugriff auf ein Sicherungs Komponenten Dokument als auch auf Writer-Metadatendokumente erforderlich. Diese Dokumente werden im Allgemeinen nicht durch Abfragen ausgelaufener Anwendungen abgerufen, sondern werden aus Versionen abgerufen, die als XML-Dokumente auf Sicherungsmedien gespeichert sind.

Wie bei Sicherungs Vorgängen, bleiben die Writer-Metadatendokumente schreibgeschützte Objekte, und (nach dem Abrufen) kann das Dokument mit den Sicherungs Komponenten dennoch geändert werden. Durch Änderungen des Dokuments mit den Sicherungs Komponenten können Writer und Anforderer über Folgendes kommunizieren:

-   Überschreiben von [*Wiederherstellungsmethoden*](vssgloss-r.md) mit [*Wiederherstellungs Zielen*](vssgloss-r.md)
-   Verwenden [ *alternativer Speicherort* Zuordnungen](vssgloss-a.md)
-   Wiederherstellen von Dateien an neuen Speicherorten auf dem Datenträger
-   Verwenden verschiedener Auswahlregeln, die bei der Sicherung verwendet werden

Zur Vereinfachung der grundlegenden Tasks, die bei einer Wiederherstellung ablaufen, wurde dieser Überblick in die folgenden Themen unterteilt:

-   [Übersicht über die Wiederherstellungs Initialisierung](overview-of-restore-initialization.md)
-   [Übersicht über das Vorbereiten der Wiederherstellung](overview-of-preparing-for-restore.md)
-   [Übersicht über die tatsächliche Dateiwiederherstellung](overview-of-actual-file-restoration.md)
-   [Übersicht über Wiederherstellungs Bereinigung und-Beendigung](overview-of-restore-clean-up-and-termination.md)

 

 



