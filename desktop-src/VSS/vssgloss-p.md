---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526279"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="74922-103">P (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="74922-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="74922-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="74922-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="74922-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**Unterstützung für Teil Dateien**</span><span class="sxs-lookup"><span data-stu-id="74922-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="74922-106">Die Kapazität zum Implementieren von Sicherungs Vorgängen durch Ändern der Unterabschnitte der beteiligten Dateien, anstatt mit den gesamten Dateien zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="74922-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="74922-107">Siehe auch [*gesteuerte Ziel Ausrichtung*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="74922-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="74922-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistente Schatten Kopie**</span><span class="sxs-lookup"><span data-stu-id="74922-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="74922-109">Eine Schatten Kopie, die nicht automatisch gelöscht wird, wenn die anfordernde Person ein [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Objekt freigibt oder wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="74922-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="74922-110">Siehe auch [*Automatische releaseschattenkopie*](vssgloss-a.md), [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="74922-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="74922-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span><span class="sxs-lookup"><span data-stu-id="74922-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="74922-112">Eine spezielle Art von Schattenkopievolume, das ein Schattenkopievolume ohne das ursprüngliche Volume vollständig und vollständig darstellt.</span><span class="sxs-lookup"><span data-stu-id="74922-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="74922-113">Dies wird auch als geteilte Spiegelung bezeichnet, in dieser Dokumentation wird jedoch der Begriff Plex verwendet.</span><span class="sxs-lookup"><span data-stu-id="74922-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="74922-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Postrestore-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74922-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="74922-115">Ein VSS-Ereignis, das angibt, dass eine VSS-Wiederherstellung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74922-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="74922-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74922-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="74922-117">Ein VSS-Ereignis, das angibt, dass eine Schatten Kopie abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="74922-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="74922-118">Siehe auch [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="74922-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="74922-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74922-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="74922-120">Ein VSS-Ereignis, das angibt, dass ein Sicherungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="74922-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="74922-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Prepareforsnapshot-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74922-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="74922-122">Ein VSS-Ereignis, das angibt, dass Writer Maßnahmen zum Vorbereiten eines bevorstehenden schattenkopievorgangs ausführen sollten.</span><span class="sxs-lookup"><span data-stu-id="74922-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="74922-123">Siehe auch [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="74922-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="74922-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74922-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="74922-125">Ein VSS-Ereignis, das angibt, dass ein Wiederherstellungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="74922-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="74922-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**ab**</span><span class="sxs-lookup"><span data-stu-id="74922-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="74922-127">Ein Betriebssystem Objekt, das e/a-Anforderungen abfängt und verwaltet, um Volumeschattenkopien im Dateisystem zu erstellen und darzustellen.</span><span class="sxs-lookup"><span data-stu-id="74922-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="74922-128">Siehe auch [*Hardware Anbieter*](vssgloss-h.md), [*Softwareanbieter*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="74922-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



