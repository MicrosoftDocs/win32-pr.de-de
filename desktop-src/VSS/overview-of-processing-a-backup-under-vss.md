---
description: Die Verarbeitung einer Sicherung, Anforderer und Writer koordiniert, um ein stabiles System Abbild bereitzustellen, von dem Daten (das schattenkopierte Volume) gesichert werden, um Dateien auf der Basis ihrer Nutzung zu gruppieren und um Informationen zu den gespeicherten Daten zu speichern.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Übersicht über die Verarbeitung einer Sicherung unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345019"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Übersicht über die Verarbeitung einer Sicherung unter VSS

Die Verarbeitung einer Sicherung, Anforderer und Writer koordiniert, um ein stabiles System Abbild bereitzustellen, von dem Daten (das schattenkopierte Volume) gesichert werden, um Dateien auf der Basis ihrer Nutzung zu gruppieren und um Informationen zu den gespeicherten Daten zu speichern. Dies muss alle durchgeführt werden, während nur minimale Unterbrechungen für den normalen Arbeitsablauf des Writers erstellt werden.

Ein Anforderer fragt Writer nach Ihren Metadaten ab, verarbeitet diese Daten, benachrichtigt die Writer vor dem Anfang der Schatten Kopie und der Sicherungs Vorgänge und benachrichtigt die Writer dann erneut, nachdem die Schattenkopie und die Sicherungs Vorgänge beendet wurden.

Als Antwort auf diese Benachrichtigungen stellt der Writer Informationen zu den zu sichernden Dateien bereit – einschließlich der Angabe von Gruppen von Dateien zur Koordinate ([*Komponenten*](vssgloss-c.md)) – hält in seinen e/a-Vorgängen vor einer Schatten Kopie an und kehrt nach dem Abschluss einer Schatten Kopie oder am Ende der Sicherung wieder zum normalen Vorgang zurück.

Im Verlauf der Verarbeitung der Sicherung gibt ein Writer die Dateien an, für die er über seine schreibgeschützten Metadaten zuständig ist – das Writer-Metadatendokument (siehe [VSS-Metadaten: Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md)). Der Anforderer interpretiert dann diese Metadaten, wählt, was gesichert werden soll, und speichert diese Entscheidungen in einem eigenen Metadatenobjekt, dem Dokument mit den Sicherungs Komponenten (siehe [VSS-Metadaten: Arbeiten mit dem Sicherungs Komponenten Dokument](working-with-the-backup-components-document.md)). Dieses Sicherungs Komponenten Dokument ist für die Überprüfung und Änderung von Writer während der Sicherungs-und Wiederherstellungs Vorgänge verfügbar.

Dieses Diagramm zeigt die Interaktionen zwischen dem Anforderer, dem VSS-Dienst, der VSS-Kernel Unterstützung, den beteiligten VSS-Writern und VSS-Hardwareanbietern.

![Interaktionen zwischen Anforderer, Sicherungs Komponenten, Writern und Anbietern](images/vssimpl.png)

Um die grundlegenden Aufgaben für die Durchführung einer Sicherung besser zu verstehen, ist es hilfreich, diese Übersicht in die folgenden Themen zu unterbrechen:

-   [Übersicht über die Initialisierung der Sicherung](overview-of-backup-initialization.md)
-   [Übersicht über die Sicherungs Ermittlungs Phase](overview-of-the-backup-discovery-phase.md)
-   [Übersicht über Aufgaben vor der Sicherung](overview-of-pre-backup-tasks.md)
-   [Übersicht über die tatsächliche Sicherung von Dateien](overview-of-actual-backup-of-files.md)
-   [Übersicht über das Beenden der Sicherung](overview-of-backup-termination.md)

 

 



