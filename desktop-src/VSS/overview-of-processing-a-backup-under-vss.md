---
description: Bei der Verarbeitung einer Sicherung koordinieren Anforderer und Writer, um ein stabiles Systemimage bereitzustellen, aus dem Daten (das Schattenkopievolume) gesichert, Dateien anhand ihrer Verwendung gruppiert und Informationen zu den gespeicherten Daten gespeichert werden.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Übersicht über die Verarbeitung einer Sicherung unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60874b1c66bcc75788912f54e5b3ffc8314f1bc0d0ad6d92b815725af727936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510010"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Übersicht über die Verarbeitung einer Sicherung unter VSS

Bei der Verarbeitung einer Sicherung koordinieren Anforderer und Writer, um ein stabiles Systemimage bereitzustellen, aus dem Daten (das Schattenkopievolume) gesichert, Dateien anhand ihrer Verwendung gruppiert und Informationen zu den gespeicherten Daten gespeichert werden. Dies muss alles geschehen, während nur eine minimale Unterbrechung des normalen Arbeitsablaufs des Writers erzeugt wird.

Ein Anforderer fragt Writer nach ihren Metadaten ab, verarbeitet diese Daten, benachrichtigt die Writer vor dem Beginn der Schattenkopie und der Sicherungsvorgänge und benachrichtigt die Writer dann erneut, nachdem die Schattenkopie- und Sicherungsvorgänge beendet wurden.

Als Reaktion auf diese Benachrichtigungen stellt der Writer Informationen zu zu sichernden Dateien bereit , einschließlich der Angabe von Gruppen von Dateien, die koordiniert werden sollen [*(Komponenten*](vssgloss-c.md)), hält in den E/A-Vorgängen vor einer Schattenkopie an und kehrt dann nach Abschluss einer Schattenkopie oder am Ende der Sicherung zum normalen Betrieb zurück.

Während der Verarbeitung der Sicherung gibt ein Writer die Dateien an, für die er über seine schreibgeschützten Metadaten verantwortlich ist – das Writer Metadata Document (siehe [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)). Der Anforderer interpretiert dann diese Metadaten, wählt aus, was gesichert werden soll, und speichert diese Entscheidungen in seinem eigenen Metadatenobjekt, dem Sicherungskomponentendokument (siehe [VSS-Metadaten: Arbeiten mit dem Sicherungskomponentendokument](working-with-the-backup-components-document.md)). Dieses Sicherungskomponentendokument ist für die Überprüfung und Änderung des Writers während der Sicherungs- und Wiederherstellungsvorgänge verfügbar.

Dieses Diagramm zeigt die Interaktionen zwischen dem Anfordernden, dem VSS-Dienst, der VSS-Kernelunterstützung, allen beteiligten VSS-Writern und allen VSS-Hardwareanbietern.

![Interaktionen zwischen Anfordernden, Sicherungskomponenten, Writern und Anbietern](images/vssimpl.png)

Um die grundlegenden Aufgaben bei der Durchführung einer Sicherung besser zu verstehen, ist es hilfreich, diese Übersicht in die folgenden Themen aufzugliedern:

-   [Übersicht über die Sicherungsinitialisierung](overview-of-backup-initialization.md)
-   [Übersicht über die Sicherungsermittlungsphase](overview-of-the-backup-discovery-phase.md)
-   [Übersicht über Aufgaben vor der Sicherung](overview-of-pre-backup-tasks.md)
-   [Übersicht über die tatsächliche Sicherung von Dateien](overview-of-actual-backup-of-files.md)
-   [Übersicht über die Beendigung von Sicherungen](overview-of-backup-termination.md)

 

 



