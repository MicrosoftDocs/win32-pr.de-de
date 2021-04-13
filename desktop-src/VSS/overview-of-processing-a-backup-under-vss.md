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
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="ecf6a-103">Übersicht über die Verarbeitung einer Sicherung unter VSS</span><span class="sxs-lookup"><span data-stu-id="ecf6a-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="ecf6a-104">Die Verarbeitung einer Sicherung, Anforderer und Writer koordiniert, um ein stabiles System Abbild bereitzustellen, von dem Daten (das schattenkopierte Volume) gesichert werden, um Dateien auf der Basis ihrer Nutzung zu gruppieren und um Informationen zu den gespeicherten Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="ecf6a-105">Dies muss alle durchgeführt werden, während nur minimale Unterbrechungen für den normalen Arbeitsablauf des Writers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="ecf6a-106">Ein Anforderer fragt Writer nach Ihren Metadaten ab, verarbeitet diese Daten, benachrichtigt die Writer vor dem Anfang der Schatten Kopie und der Sicherungs Vorgänge und benachrichtigt die Writer dann erneut, nachdem die Schattenkopie und die Sicherungs Vorgänge beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="ecf6a-107">Als Antwort auf diese Benachrichtigungen stellt der Writer Informationen zu den zu sichernden Dateien bereit – einschließlich der Angabe von Gruppen von Dateien zur Koordinate ([*Komponenten*](vssgloss-c.md)) – hält in seinen e/a-Vorgängen vor einer Schatten Kopie an und kehrt nach dem Abschluss einer Schatten Kopie oder am Ende der Sicherung wieder zum normalen Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="ecf6a-108">Im Verlauf der Verarbeitung der Sicherung gibt ein Writer die Dateien an, für die er über seine schreibgeschützten Metadaten zuständig ist – das Writer-Metadatendokument (siehe [VSS-Metadaten: Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="ecf6a-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="ecf6a-109">Der Anforderer interpretiert dann diese Metadaten, wählt, was gesichert werden soll, und speichert diese Entscheidungen in einem eigenen Metadatenobjekt, dem Dokument mit den Sicherungs Komponenten (siehe [VSS-Metadaten: Arbeiten mit dem Sicherungs Komponenten Dokument](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="ecf6a-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="ecf6a-110">Dieses Sicherungs Komponenten Dokument ist für die Überprüfung und Änderung von Writer während der Sicherungs-und Wiederherstellungs Vorgänge verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="ecf6a-111">Dieses Diagramm zeigt die Interaktionen zwischen dem Anforderer, dem VSS-Dienst, der VSS-Kernel Unterstützung, den beteiligten VSS-Writern und VSS-Hardwareanbietern.</span><span class="sxs-lookup"><span data-stu-id="ecf6a-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![Interaktionen zwischen Anforderer, Sicherungs Komponenten, Writern und Anbietern](images/vssimpl.png)

<span data-ttu-id="ecf6a-113">Um die grundlegenden Aufgaben für die Durchführung einer Sicherung besser zu verstehen, ist es hilfreich, diese Übersicht in die folgenden Themen zu unterbrechen:</span><span class="sxs-lookup"><span data-stu-id="ecf6a-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="ecf6a-114">Übersicht über die Initialisierung der Sicherung</span><span class="sxs-lookup"><span data-stu-id="ecf6a-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="ecf6a-115">Übersicht über die Sicherungs Ermittlungs Phase</span><span class="sxs-lookup"><span data-stu-id="ecf6a-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="ecf6a-116">Übersicht über Aufgaben vor der Sicherung</span><span class="sxs-lookup"><span data-stu-id="ecf6a-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="ecf6a-117">Übersicht über die tatsächliche Sicherung von Dateien</span><span class="sxs-lookup"><span data-stu-id="ecf6a-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="ecf6a-118">Übersicht über das Beenden der Sicherung</span><span class="sxs-lookup"><span data-stu-id="ecf6a-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



