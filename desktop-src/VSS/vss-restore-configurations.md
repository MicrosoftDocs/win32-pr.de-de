---
description: Die Dateiwiederherstellung auf einem laufenden System kann problematisch sein. Es ist wichtig, dass ausgestellte Anwendungen (Writer) angeben, was zu tun ist, wenn während der Wiederherstellung Probleme auftreten, beispielsweise, wenn die wieder herzustellende Datei zurzeit verwendet wird.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: VSS-Wiederherstellungs Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129293"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="7aa69-104">VSS-Wiederherstellungs Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="7aa69-104">VSS Restore Configurations</span></span>

<span data-ttu-id="7aa69-105">Die Dateiwiederherstellung auf einem laufenden System kann problematisch sein.</span><span class="sxs-lookup"><span data-stu-id="7aa69-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="7aa69-106">Es ist wichtig, dass ausgestellte Anwendungen (Writer) angeben, was zu tun ist, wenn während der Wiederherstellung Probleme auftreten, beispielsweise, wenn die wieder herzustellende Datei zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa69-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="7aa69-107">Unter VSS haben Writer zwei ergänzende Möglichkeiten zur Verwaltung von [*Wiederherstellungen – Wiederherstellungsmethoden*](vssgloss-r.md) und [*Wiederherstellungs Ziele*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="7aa69-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="7aa69-108">Außerdem können Anforderer die Dateien an zuvor nicht angegebenen Speicherorten wiederherstellen und Writer Benachrichtigen (Weitere Informationen finden Sie unter [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="7aa69-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="7aa69-109">Die Restore-Methode (auch das ursprüngliche Wiederherstellungs Ziel) wird von einem Writer zum Zeitpunkt der Sicherung angegeben und legt eine Writer-weite Definition der Methode fest, die zum Wiederherstellen aller ihrer Komponenten in der Zukunft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7aa69-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="7aa69-110">Alle Dateien und Komponenten, die von einem Writer verwaltet werden, verwenden dieselbe Wiederherstellungsmethode.</span><span class="sxs-lookup"><span data-stu-id="7aa69-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="7aa69-111">Mit Wiederherstellungs Zielen können Writer die Art und Weise ändern, wie bestimmte Komponenten zum Zeitpunkt der Wiederherstellung wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7aa69-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="7aa69-112">Im Gegensatz zu Restore-Methoden werden Wiederherstellungs Ziele für einen Komponenten Satz definiert.</span><span class="sxs-lookup"><span data-stu-id="7aa69-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="7aa69-113">Eine ausführliche Erläuterung der Verwendung von Wiederherstellungsmethoden und Wiederherstellungs Zielen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7aa69-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="7aa69-114">VSS-Wiederherstellungs Status</span><span class="sxs-lookup"><span data-stu-id="7aa69-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="7aa69-115">Festlegen von VSS-Wiederherstellungsmethoden</span><span class="sxs-lookup"><span data-stu-id="7aa69-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="7aa69-116">Festlegen von VSS-Wiederherstellungs Zielen</span><span class="sxs-lookup"><span data-stu-id="7aa69-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="7aa69-117">Festlegen der VSS-Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="7aa69-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="7aa69-118">(Informationen zu Wiederherstellungen, bei denen diese Mechanismen nicht verwendet werden, finden Sie unter wieder [herstellen ohne Writer-Teilnahme](restores-without-writer-participation.md).)</span><span class="sxs-lookup"><span data-stu-id="7aa69-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



