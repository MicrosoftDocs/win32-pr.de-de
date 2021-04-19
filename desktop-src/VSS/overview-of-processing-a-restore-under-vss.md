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
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="4c64e-103">Übersicht über die Verarbeitung einer Wiederherstellung unter VSS</span><span class="sxs-lookup"><span data-stu-id="4c64e-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="4c64e-104">Bei der Verarbeitung einer Sicherung unter VSS haben Anforderer und Writer zusammengearbeitet, um ein stabiles System Abbild zu erstellen, mit dem die Daten gesichert werden müssen, wofür eine Koordination und Erstellung einer Schatten Kopie des aktuellen Systems erforderlich war.</span><span class="sxs-lookup"><span data-stu-id="4c64e-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="4c64e-105">Anders als bei einer VSS-Sicherung, bei der der Zweck der Koordination von Anforderer und Writer darin besteht, ein stabiles System Abbild zu erstellen, aus dem Daten kopiert werden sollen, besteht das Ziel einer VSS-basierten Wiederherstellung darin, Dateien auf eine Weise zurückzugeben, die für Anwendungen (Writer), die derzeit im System ausgeführt werden, am nützlichsten</span><span class="sxs-lookup"><span data-stu-id="4c64e-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="4c64e-106">Dies erfordert kein stabiles System Abbild, sodass keine Schatten Kopie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4c64e-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="4c64e-107">Stattdessen konzentriert sich der Schwerpunkt auf die Vermeidung von Unterbrechungen der Schreiber Aktivität, verhindert das Erstellen inkonsistenter Datasets auf dem Datenträger und ermöglicht es den Writern, bei Bedarf Daten auszuwerten und zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="4c64e-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="4c64e-108">Wie bei einem Sicherungs Vorgang ist für eine VSS-Wiederherstellung sowohl der Zugriff auf ein Sicherungs Komponenten Dokument als auch auf Writer-Metadatendokumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4c64e-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="4c64e-109">Diese Dokumente werden im Allgemeinen nicht durch Abfragen ausgelaufener Anwendungen abgerufen, sondern werden aus Versionen abgerufen, die als XML-Dokumente auf Sicherungsmedien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4c64e-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="4c64e-110">Wie bei Sicherungs Vorgängen, bleiben die Writer-Metadatendokumente schreibgeschützte Objekte, und (nach dem Abrufen) kann das Dokument mit den Sicherungs Komponenten dennoch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4c64e-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="4c64e-111">Durch Änderungen des Dokuments mit den Sicherungs Komponenten können Writer und Anforderer über Folgendes kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="4c64e-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="4c64e-112">Überschreiben von [*Wiederherstellungsmethoden*](vssgloss-r.md) mit [*Wiederherstellungs Zielen*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="4c64e-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="4c64e-113">Verwenden [ *alternativer Speicherort* Zuordnungen](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="4c64e-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="4c64e-114">Wiederherstellen von Dateien an neuen Speicherorten auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="4c64e-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="4c64e-115">Verwenden verschiedener Auswahlregeln, die bei der Sicherung verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4c64e-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="4c64e-116">Zur Vereinfachung der grundlegenden Tasks, die bei einer Wiederherstellung ablaufen, wurde dieser Überblick in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="4c64e-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="4c64e-117">Übersicht über die Wiederherstellungs Initialisierung</span><span class="sxs-lookup"><span data-stu-id="4c64e-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="4c64e-118">Übersicht über das Vorbereiten der Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="4c64e-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="4c64e-119">Übersicht über die tatsächliche Dateiwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="4c64e-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="4c64e-120">Übersicht über Wiederherstellungs Bereinigung und-Beendigung</span><span class="sxs-lookup"><span data-stu-id="4c64e-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



