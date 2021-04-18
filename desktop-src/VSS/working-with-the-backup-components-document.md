---
description: Ein Anforderer erstellt ein Sicherungs Komponenten Dokument zu Beginn der Sicherung.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Arbeiten mit dem Dokument mit den Sicherungs Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347183"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="63076-103">Arbeiten mit dem Dokument mit den Sicherungs Komponenten</span><span class="sxs-lookup"><span data-stu-id="63076-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="63076-104">Ein Anforderer erstellt ein Sicherungs Komponenten Dokument zu Beginn der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="63076-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="63076-105">Das Dokument enthält zunächst nur eine Beschreibung des Status des Sicherungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="63076-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="63076-106">Während der Wiederherstellung sollte das Dokument Anweisungen dazu bereitstellen, wie ein Anforderer mit dem Kopieren von Dateien auf den Datenträger fortfahren soll.</span><span class="sxs-lookup"><span data-stu-id="63076-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="63076-107">Im Verlauf des Wiederherstellungs Vorgangs wird das Dokument mit den Sicherungs Komponenten geändert, das den Status dieses Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="63076-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="63076-108">Im Gegensatz zum schreibgeschützten Writer-Metadatendokument gibt es ein Fenster, in dem das Dokument mit den Sicherungs Komponenten von Anforderern und Writern geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="63076-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="63076-109">Das Dokument kann bis zur Generierung eines [*BackupComplete*](vssgloss-b.md) -oder [*BackupShutdown*](vssgloss-b.md) -Ereignisses während Sicherungs Vorgängen und bis zu einem [*postrestore*](vssgloss-p.md) -Ereignis während der Wiederherstellung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="63076-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="63076-110">Um das Dokument mit den Sicherungs Komponenten eines Anforderers zu verwenden, ist ein Verständnis der folgenden Themen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="63076-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="63076-111">Lebenszyklus von Sicherungs Komponenten Dokumenten</span><span class="sxs-lookup"><span data-stu-id="63076-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="63076-112">Dokumentinhalte der Sicherungs Komponenten</span><span class="sxs-lookup"><span data-stu-id="63076-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



