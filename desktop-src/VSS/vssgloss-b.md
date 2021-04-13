---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343569"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="0741b-103">B (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="0741b-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="0741b-104">[a](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="0741b-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0741b-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**Anwendungen auf Back-End-Ebene**</span><span class="sxs-lookup"><span data-stu-id="0741b-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-106">Gibt den Punkt an, an dem ein Writer über eine Sperre durch den VSS benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0741b-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="0741b-107">Writer, die als Back-End-Anwendungen initialisiert werden, werden benachrichtigt, nachdem Writer als Anwendungen auf Front-End-Ebene initialisiert wurden und bevor Sie als Anwendungen auf Systemebene initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0741b-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="0741b-108">Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Front-End-Anwendungen*](vssgloss-f.md), Anwendungen auf [*Systemebene*](vssgloss-s.md)und [*Writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="0741b-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="0741b-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0741b-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-110">Ein VSS-Ereignis, das angibt, dass eine VSS-Sicherung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0741b-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="0741b-111">Auf dieses Ereignis sollte ein BackupShutdown-Ereignis im normalen Betrieb folgen.</span><span class="sxs-lookup"><span data-stu-id="0741b-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="0741b-112">Siehe auch *BackupShutdown-Ereignis*.</span><span class="sxs-lookup"><span data-stu-id="0741b-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="0741b-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Dokument mit Sicherungs Komponenten**</span><span class="sxs-lookup"><span data-stu-id="0741b-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-114">Ein XML-Dokument, das von einem Anforderer (mithilfe der **IVssBackupComponents** -Schnittstelle) im Rahmen der Einrichtung eines Wiederherstellungs-oder Sicherungs Vorgangs erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0741b-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="0741b-115">Das Sicherungskomponentendokument enthält eine Liste der Komponenten, die von mindestens einem Writer, der an einem Sicherungs- oder Wiederherstellungsvorgang beteiligt ist, explizit hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0741b-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="0741b-116">Es enthält keine implizit enthaltenen Komponenteninformationen.</span><span class="sxs-lookup"><span data-stu-id="0741b-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="0741b-117">Ein Writer-Metadatendokument enthält nur Writer-Komponenten, die an einer Sicherung beteiligt sein können.</span><span class="sxs-lookup"><span data-stu-id="0741b-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="0741b-118">Ein Sicherungs Komponenten Dokument kann auf einem Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0741b-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="0741b-119">Siehe auch [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="0741b-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="0741b-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**Sicherungs Satz**</span><span class="sxs-lookup"><span data-stu-id="0741b-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-121">Die zu sichernden Dateien.</span><span class="sxs-lookup"><span data-stu-id="0741b-121">Those files to be backed up.</span></span> <span data-ttu-id="0741b-122">Es umfasst Dateien, die durch einschließen in eine Komponente ausgewählt werden, und die von include-Anweisungen auf Writer-Ebene angegeben werden, weniger die explizit enthaltenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="0741b-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="0741b-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0741b-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-124">Ein VSS-Ereignis, das angibt, dass eine kompatible Sicherungs Anwendung heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="0741b-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="0741b-125">Normalerweise wird diesem ein BackupComplete-Ereignis vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="0741b-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="0741b-126">Wenn eine Sicherung jedoch unerwartet beendet wird, kann dieses Ereignis ohne ein vorangestelltem BackupComplete-Ereignis generiert werden.</span><span class="sxs-lookup"><span data-stu-id="0741b-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="0741b-127">Siehe auch *BackupComplete-Ereignis*.</span><span class="sxs-lookup"><span data-stu-id="0741b-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="0741b-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**Sicherungs Stempel**</span><span class="sxs-lookup"><span data-stu-id="0741b-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="0741b-129">Eine Zeichenfolge, die Informationen zu dem Zeitpunkt enthält, zu dem eine Sicherung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="0741b-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="0741b-130">VSS legt keine Einschränkung für das Format dieser Zeichenfolge fest, mit dem Unterschied, dass es für alle Writer-Instanzen einer bestimmten Klasse verständlich ist.</span><span class="sxs-lookup"><span data-stu-id="0741b-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="0741b-131">Sie enthält möglicherweise Zeit-und Datumsinformationen, logische Sequenznummern oder andere Informationen, die es einem Writer der gleichen Klasse ermöglichen, zu bestimmen, wann die letzte Sicherung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="0741b-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



