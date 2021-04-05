---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751544"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="b30ce-103">F (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="b30ce-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="b30ce-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="b30ce-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b30ce-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**Dateigruppen Komponente**</span><span class="sxs-lookup"><span data-stu-id="b30ce-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-106">Eine Gruppe von Dateien, die nicht als Datenbank verwendet und von einem Writer definiert werden, da Sie während Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b30ce-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="b30ce-107">Siehe auch [*Komponente*](vssgloss-c.md), [*Datenbankkomponente*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="b30ce-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**Dateisatz**</span><span class="sxs-lookup"><span data-stu-id="b30ce-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-109">Die Kombination aus einem Pfad, einer Datei Spezifikation und einem rekursiven Flag, das eine Datei oder eine Gruppe von Dateien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b30ce-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="b30ce-110">Dateien werden z. b. den Komponenten in Datei Sätzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b30ce-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="b30ce-111">Sofern nicht anders angegeben, sind die Pfade eines Datei Satzes standardmäßige Windows-Pfade und können Umgebungsvariablen (z. b .% systemroot%) enthalten. darf jedoch keine Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b30ce-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="b30ce-112">Es ist nicht erforderlich, dass der Pfad mit einem umgekehrten Schrägstrich (" \\ ") endet.</span><span class="sxs-lookup"><span data-stu-id="b30ce-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="b30ce-113">Es gibt Anwendungen, die diese Informationen abrufen, um Sie zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b30ce-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="b30ce-114">Die in einem Datei Satz enthaltene Datei Spezifikation gibt den Namen der Datei oder Dateien an, die Sie enthält.</span><span class="sxs-lookup"><span data-stu-id="b30ce-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="b30ce-115">Diese Datei Spezifikation darf keine Verzeichnis Spezifikationen (z. b. keine umgekehrten Schrägstriche) enthalten, kann aber auch das enthalten?</span><span class="sxs-lookup"><span data-stu-id="b30ce-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="b30ce-116">und Platzhalter \* Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b30ce-116">and \* wildcard characters.</span></span>

<span data-ttu-id="b30ce-117">Das rekursive Tag ist ein boolescher Wert, der angibt, ob der Pfad des Datei Satzes als nur ein einzelnes Verzeichnis behandelt werden soll oder ob er eine Hierarchie von Verzeichnissen angibt, die rekursiv durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b30ce-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="b30ce-118">Der boolesche Wert ist **true** , wenn der Pfad als eine Hierarchie von Verzeichnissen behandelt wird, die rekursiv durchlaufen werden sollen, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b30ce-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="b30ce-119">Informationen zu einem Dateisatz werden durch Instanzen der **ivsswmfiledesc** -Schnittstelle zurückgegeben und können zusätzliche Informationen enthalten, einschließlich alternativer Pfade, alternativer Speicherort Zuordnungen und Schema Unterstützungs Einstellungen auf Dateiebene.</span><span class="sxs-lookup"><span data-stu-id="b30ce-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="b30ce-120">Siehe auch [*Alternativer Pfad*](vssgloss-a.md), [*Zuordnung alternativer Speicherorte*](vssgloss-a.md), [*Komponente*](vssgloss-c.md), *Datei Spezifikation*.</span><span class="sxs-lookup"><span data-stu-id="b30ce-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Datei Spezifikation**</span><span class="sxs-lookup"><span data-stu-id="b30ce-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-122">Wird verwendet, um Dateien innerhalb eines Verzeichnisses abzugleichen und einen Datei Satz zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b30ce-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="b30ce-123">Er darf keine Verzeichnis Spezifikationen (z. b. keine umgekehrten Schrägstriche) enthalten, kann aber auch das enthalten?</span><span class="sxs-lookup"><span data-stu-id="b30ce-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="b30ce-124">und Platzhalter \* Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b30ce-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Datei Replikations Dienst**</span><span class="sxs-lookup"><span data-stu-id="b30ce-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-126">Wird verwendet, um Systemdateien in einem SYSVOL-Verzeichnis (Redundant System Volume) zu replizieren, um die Survivability des Dateisystems zu unterstützen, insbesondere für verteilte Dateisysteme.</span><span class="sxs-lookup"><span data-stu-id="b30ce-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**ge**</span><span class="sxs-lookup"><span data-stu-id="b30ce-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-128">Ein Zeitraum während des Erstellungs Prozesses der Schatten Kopie, wenn alle Writer ihre Schreibvorgänge auf die Volumes geleert haben und keine weiteren Schreibvorgänge einleiten.</span><span class="sxs-lookup"><span data-stu-id="b30ce-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Ereignis Einfrieren**</span><span class="sxs-lookup"><span data-stu-id="b30ce-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-130">Ein VSS-Ereignis, das angibt, dass eine schattenkopiesperre ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b30ce-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="b30ce-131">Siehe auch *Einfrieren*, [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b30ce-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30ce-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**Anwendungen auf Front-End-Ebene**</span><span class="sxs-lookup"><span data-stu-id="b30ce-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="b30ce-133">Gibt den Punkt an, an dem ein Writer über eine Sperre durch den VSS benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b30ce-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="b30ce-134">Writer, die als Anwendungen auf Front-End-Ebene initialisiert wurden, werden vor Writer benachrichtigt, die als Back-End-Ebene-Anwendungen oder als Anwendungen auf Systemebene initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b30ce-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="b30ce-135">Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Back-End-Anwendungen*](vssgloss-b.md), Anwendungen auf [*Systemebene*](vssgloss-s.md)und [*Writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="b30ce-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



