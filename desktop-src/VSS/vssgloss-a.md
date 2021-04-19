---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359841"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="ca3e6-103">A (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="ca3e6-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ca3e6-104">a [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ca3e6-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ca3e6-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abbruch Ereignis**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-106">Ein vom Volumeschattenkopie-Dienst ausgestelltes VSS-Ereignis, das angibt, dass ein kompatibler Sicherungs-oder Wiederherstellungs Vorgang abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="ca3e6-107">Der Ereignishandler ist **CVssWriter:: OnAbort**.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-109">Bei Active Directory Service (ADSI) handelt es sich um einen com-basierten Dienst, der einen Mechanismus zum Suchen, identifizieren und Zugreifen auf die Benutzer und Ressourcen bereitstellt, die in einem verteilten Computer Umgebungs System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="ca3e6-110">Insbesondere wird der Active Directory-Dienst zum Verwalten von Enterprise-Verzeichnisinformationen für die Verteilung durch einen Windows-Domänen Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**Zuordnung alternativer Speicherorte**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-112">Ein Pfad, der nicht der ursprüngliche Pfad einer Datei ist, in den die Datei unter bestimmten Bedingungen wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="ca3e6-113">In der Regel sind alternative Speicherort Zuordnungen nicht für eine einzelne klar definierte Datei definiert, sondern für ein Pfad-/dateispezifikations-paar und können rekursiv sein.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="ca3e6-114">Eine Alternative Speicherort Zuordnung wird nur während eines Wiederherstellungs Vorgangs verwendet und sollte nicht mit einem alternativen Pfad verwechselt werden, der nur während eines Sicherungs Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="ca3e6-115">Siehe auch *Alternativer Pfad*.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**Alternativer Pfad**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-117">Bei Sicherungs Vorgängen weist ein Pfad-/dateispezifikations-Paar (das von einer Instanz der **ivsswmfiledesc** -Schnittstelle verarbeitet wird) einen alternativen Pfad auf, wenn der zugehörige Dateideskriptor (wie von **ivsswmfiledesc:: getalternateloation** zurückgegeben) nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="ca3e6-118">Der Pfad ist von diesem Pfad und nicht vom standardmäßigen angegebenen Pfad. diese Dateien müssen bei der Sicherung eines Volumes kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="ca3e6-119">Ein alternativer Pfad wird nur während eines Sicherungs Vorgangs verwendet und sollte nicht mit einer alternativen Speicherort Zuordnung verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="ca3e6-120">Eine Alternative Speicherort Zuordnung wird nur bei Wiederherstellungs Vorgängen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="ca3e6-121">Siehe auch *Alternative Speicherort Zuordnung*.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**Anwendungsebene**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-123">Wird von VSS verwendet, um den Punkt im Verlauf der Erstellung einer Schatten Kopie anzugeben, die ein Writer über einen Einfrieren benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="ca3e6-124">Weitere Informationen finden Sie unter [*Anwendungen auf Back-End-Ebene*](vssgloss-b.md), [*Einfrieren*](vssgloss-f.md), [*Front-End-Anwendungen*](vssgloss-f.md), [*Schatten Kopie*](vssgloss-s.md), [*Anwendungen auf Systemebene*](vssgloss-s.md), [*Writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="ca3e6-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**automatisch wiederhergestellte Schatten Kopie**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-126">Eine Schatten Kopie, bei der eine zusätzliche Verarbeitung durch einen Writer in einem vollständig konsistenten Zustand für Sicherungs-oder Data Mining Aktionen aufgetreten ist (z. b. ein Rollback aller Transaktionen, die noch nicht abgeschlossen wurden, während die Schatten Kopie erstellt wurde). Dies kann durch einen Writer initiiert werden, indem Sie ein entsprechendes Flag aus der **VSS- \_ \_ Komponentenflags** -Enumeration im **dwcomponentflags** -Member der **VSS \_ ComponentInfo** -Struktur oder durch einen Anforderer angeben, indem Sie dem Kontext für die Schatten Kopie das **VSS- \_ Volsnap \_ attr- \_ Rollback- \_ Wiederherstellungsflag** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="ca3e6-127">Die automatische Wiederherstellung ermöglicht die Verwendung der schattenkopierten Daten auf einem schreibgeschützten Volume, für Data Mining, für Teil Wiederherstellungen (z. b. ausgewählte Elemente in einer Datenbank) oder für andere Zwecke.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="ca3e6-128">Siehe auch [*austauschen Shadow Copy*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="ca3e6-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca3e6-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**Schatten Kopie automatisch freigeben**</span><span class="sxs-lookup"><span data-stu-id="ca3e6-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ca3e6-130">Eine Schatten Kopie, die bei Beendigung eines Sicherungs Vorgangs gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="ca3e6-131">Programm gesteuert bedeutet dies, dass die Schatten Kopie gelöscht wird, wenn die **IVssBackupComponents** -Schnittstelle freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="ca3e6-132">Eine automatische releaseschattenkopie kann nicht persistent sein.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="ca3e6-133">Standardmäßig werden alle Schatten Kopien automatisch veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ca3e6-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="ca3e6-134">Siehe auch [*persistente Schatten Kopie*](vssgloss-p.md), [*austauschen-Schatten Kopie*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="ca3e6-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



