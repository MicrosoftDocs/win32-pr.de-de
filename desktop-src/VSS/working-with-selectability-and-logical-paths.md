---
description: Die Teilnahme eines Writers an einem Sicherungs-oder Wiederherstellungs Vorgang und der Daten, die gespeichert werden, hängt davon ab, welche Komponenten explizit als Teil des Dokuments der Sicherungs Komponenten eines Anforderers und der Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten innerhalb des Writer-Metadatendokuments enthalten sind.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Arbeiten mit selekabilität und logischen Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360043"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="71203-103">Arbeiten mit selekabilität und logischen Pfaden</span><span class="sxs-lookup"><span data-stu-id="71203-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="71203-104">Die Teilnahme eines Writers an einem Sicherungs-oder Wiederherstellungs Vorgang und der Daten, die gespeichert werden, hängt davon ab, welche Komponenten [*explizit*](vssgloss-e.md) als Teil des Dokuments der Sicherungs Komponenten eines Anforderers und der Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten innerhalb des Writer-Metadatendokuments enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="71203-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="71203-105">Writer ohne Komponenten, die vor der Generierung eines [*PrepareForBackup*](vssgloss-p.md) -Ereignisses (im Fall von Sicherungs Vorgängen) oder eines [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Ereignisses (bei Wiederherstellungs Vorgängen) zum Sicherungs Komponenten Dokument eines Anforderers hinzugefügt wurden, erhalten nach diesem Zeitpunkt keine Ereignisse und werden nicht an dem Sicherungs-oder Wiederherstellungs Vorgang beteiligt.</span><span class="sxs-lookup"><span data-stu-id="71203-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="71203-106">Die Freiheit eines Anforderers, eine bestimmte Komponente in eine Sicherung oder Wiederherstellung einzubeziehen oder auszuschließen, wird jedoch durch Folgendes gesteuert:</span><span class="sxs-lookup"><span data-stu-id="71203-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="71203-107">Jede Hierarchie, die zwischen den von einem Writer verwalteten Komponenten besteht und durch [ *logische Pfade* ausgedrückt wird](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="71203-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="71203-108">Gibt an, ob die Komponente [ *für die Sicherung ausgewählt* werden soll.](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="71203-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="71203-109">Gibt an, ob es [ *für die Wiederherstellung ausgewählt* ist.](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="71203-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="71203-110">Gibt an, ob eine explizite Abhängigkeit zwischen einer bestimmten Komponente in einem bestimmten Writer und anderen Komponenten in anderen Writern vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="71203-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="71203-111">Weitere Informationen zu diesen Problemen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="71203-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="71203-112">Logische Komponente von Komponenten</span><span class="sxs-lookup"><span data-stu-id="71203-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="71203-113">Arbeiten mit selekabilität für die Sicherung</span><span class="sxs-lookup"><span data-stu-id="71203-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="71203-114">Arbeiten mit selekabilität für die Wiederherstellung und unter Komponenten</span><span class="sxs-lookup"><span data-stu-id="71203-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="71203-115">Selekabilität und arbeiten mit Komponenteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="71203-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="71203-116">Abhängigkeiten zwischen Komponenten, die von unterschiedlichen Writern verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="71203-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



