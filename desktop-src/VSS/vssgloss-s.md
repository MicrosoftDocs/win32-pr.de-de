---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345068"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="51084-103">S (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="51084-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="51084-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="51084-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="51084-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selekabilität für Sicherung**</span><span class="sxs-lookup"><span data-stu-id="51084-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="51084-106">Eine Komponente kann für die Sicherung ausgewählt werden, wenn die explizite Einbindung in einen Sicherungs Vorgang optional ist.</span><span class="sxs-lookup"><span data-stu-id="51084-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="51084-107">Die selectlichkeit der Sicherung ist aktiviert, wenn der Wert des **bwählbaren** Members der [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur **true** ist.</span><span class="sxs-lookup"><span data-stu-id="51084-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="51084-108">Es ist kein Standardwert für die selekabilität einer Komponente für die Sicherung vorhanden. ein Writer muss diesen Wert immer explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="51084-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="51084-109">Writer verwenden auch selectlichkeit für die Wiederherstellung, um die Beteiligung der Komponente an Wiederherstellungs Vorgängen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="51084-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="51084-110">Weitere Informationen finden Sie unter *auswählbare Komponente*, *Auswahlmöglichkeit für die Wiederherstellung*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*implizite Komponenten Einbindung*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="51084-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selekabilität für die Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="51084-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="51084-112">Eine Komponente kann für die Wiederherstellung ausgewählt werden, wenn Sie implizit als Teil eines Komponenten Satzes gesichert werden kann, und später einzeln ohne den Rest des Komponenten Satzes wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="51084-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="51084-113">Die Auswahlfunktion für die Wiederherstellung ist aktiviert, wenn der Wert des **bselectableforrestore** -Members der [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="51084-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="51084-114">Standardmäßig ist die Wählbarkeit einer Komponente für Restore auf **false**.</span><span class="sxs-lookup"><span data-stu-id="51084-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="51084-115">Die Auswahl für die Wiederherstellung ist nur dann von Bedeutung, wenn eine Komponente nicht zum Sicherungs Dokument hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="51084-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="51084-116">Weitere Informationen finden Sie unter *auswählbare Komponente*, *Auswahlmöglichkeit für Sicherungen*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="51084-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**auswählbare Komponente**</span><span class="sxs-lookup"><span data-stu-id="51084-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="51084-118">Eine Komponente wird als auswählbar bezeichnet, wenn die explizite Einbindung in einen Sicherungs-oder Wiederherstellungs Vorgang optional ist.</span><span class="sxs-lookup"><span data-stu-id="51084-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="51084-119">Die Auswahl der für die Wiederherstellung von Sicherungs-und Auswahl Optionen ist unabhängig voneinander – eine Komponente kann für beide Vorgänge, für die Wiederherstellung, nicht für Sicherungen oder für Sicherungen und nicht für die Wiederherstellung auswählbar sein.</span><span class="sxs-lookup"><span data-stu-id="51084-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="51084-120">Writer verwenden auch selectlichkeit, um Ihre Komponenten in Gruppen zu organisieren:</span><span class="sxs-lookup"><span data-stu-id="51084-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="51084-121">Nicht auswählbare Komponenten ohne auswählbare Vorgänger in ihren logischen Pfaden müssen immer explizit eingeschlossen werden, wenn ein Writer gesichert oder wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51084-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="51084-122">Nicht auswählbare Komponenten mit auswählbaren Vorgängern werden nur in eine Sicherung oder Wiederherstellung eingeschlossen, wenn mindestens ein auswählbarer Vorgänger eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="51084-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="51084-123">Auswählbare Komponenten ohne auswählbare Vorgänger können nur explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="51084-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="51084-124">Auswählbare Komponenten mit auswählbaren Vorgängern können explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden, oder Sie können implizit eingeschlossen werden, wenn einer ihrer auswählbaren Vorgänger eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="51084-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="51084-125">Weitere Informationen finden Sie unter [*Komponenten*](vssgloss-c.md), *selectlichkeit für Sicherung*, *selektbarkeit für die Wiederherstellung*, [*explizite Komponenten Einbindung*](vssgloss-e.md), [*implizite Komponenten Einbindung*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="51084-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**Schatten Kopie**</span><span class="sxs-lookup"><span data-stu-id="51084-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="51084-127">Ein Schreib geschütztes Zeit Punkt Replikat des Inhalts eines ursprünglichen Volumes.</span><span class="sxs-lookup"><span data-stu-id="51084-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="51084-128">Jede Schatten Kopie wird mit einer permanenten GUID verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="51084-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="51084-129">Wird auch als Volumeschattenkopie bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="51084-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="51084-130">Siehe auch *Schattenkopiesatz*.</span><span class="sxs-lookup"><span data-stu-id="51084-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="51084-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Schattenkopien für freigegebene Ordner**</span><span class="sxs-lookup"><span data-stu-id="51084-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="51084-132">Ein Windows-Feature, das mithilfe von VSS Lightweight-, Online-Sicherungskopien von Volumes erstellt.</span><span class="sxs-lookup"><span data-stu-id="51084-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="51084-133">Clients können über die Windows-Shell auf diese Sicherungen zugreifen, um alte Versionen von Dateien anzuzeigen und Fehler rückgängig zu machen, ohne eine vollständige Wiederherstellung zu erfordern</span><span class="sxs-lookup"><span data-stu-id="51084-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="51084-134">Siehe auch zum [*Client zugänglichen Schatten Kopie*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="51084-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**Schattenkopiesatz**</span><span class="sxs-lookup"><span data-stu-id="51084-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="51084-136">Eine Auflistung von Volumeschattenkopien, die gleichzeitig erstellt und durch eine gemeinsame Schattenkopiesatz-ID (einen persistenten GUID-Wert) identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="51084-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="51084-137">Dies ist der Mechanismus, der verwendet wird, um die Verwaltung eines schattenkopiervorgangs auf mehreren Volumes zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="51084-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="51084-138">Siehe auch *Schatten Kopie*.</span><span class="sxs-lookup"><span data-stu-id="51084-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="51084-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**Softwareanbieter**</span><span class="sxs-lookup"><span data-stu-id="51084-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="51084-140">Ein Anbieter, der e/a-Anforderungen auf Software Ebene zwischen dem Dateisystem und dem Volumemanager abfängt.</span><span class="sxs-lookup"><span data-stu-id="51084-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="51084-141">Siehe auch [*Hardware Anbieter*](vssgloss-h.md), [*Anbieter*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="51084-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Unterkomponente**</span><span class="sxs-lookup"><span data-stu-id="51084-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="51084-143">Jede Komponente, die über einen logischen Pfad verfügt, der eine auswählbare (für die Sicherung oder Wiederherstellung) übergeordnete Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="51084-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="51084-144">Unter Komponenten müssen einen logischen Pfad in der Form {Component \_ Name} \\ {subcomponent \_ Name} aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51084-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="51084-145">Wenn eine der auswählbaren (für Sicherungs-oder Wiederherstellungs Vorgänger) Komponenten explizit in eine Sicherung oder Wiederherstellung eingeschlossen ist, wird die Unterkomponente implizit in den Vorgang eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51084-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="51084-146">Implizit enthaltene unter Komponenten enthalten keine Daten im Sicherungs Komponenten Dokument – unabhängig davon, ob Sie ausgewählt werden können (entweder bei der Wiederherstellung oder bei der Sicherung).</span><span class="sxs-lookup"><span data-stu-id="51084-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="51084-147">Siehe auch [*Komponente*](vssgloss-c.md), [*logischer Pfad*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="51084-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**schattenkopieschattenkopie**</span><span class="sxs-lookup"><span data-stu-id="51084-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="51084-149">Ein schattenkopiertes Volume, das für den Mount Manager-Namespace eines Systems sichtbar ist – dies bedeutet, dass **findfirstvolume** und **findnextvolume** es finden können und dass Volumen-und Abbruch Benachrichtigungen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="51084-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="51084-150">Alle verfügbar gemachten Schatten Kopien sind auch Schatten Kopien.</span><span class="sxs-lookup"><span data-stu-id="51084-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="51084-151">Allerdings muss eine aufgeschietete Schatten Kopie nicht verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="51084-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="51084-152">Wenn eine Schatten Kopie transportierbar ist, kann Sie nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51084-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="51084-153">Siehe auch verfügbar gemachte [*Schatten Kopie*](vssgloss-e.md), [*austauschen-Schatten Kopie*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="51084-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System Datei Schutz**</span><span class="sxs-lookup"><span data-stu-id="51084-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="51084-155">Siehe [*Windows-Datei Schutz*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="51084-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**Anwendungen auf Systemebene**</span><span class="sxs-lookup"><span data-stu-id="51084-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="51084-157">Gibt den Punkt an, an dem VSS einen Writer über eine Sperrung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="51084-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="51084-158">Writer, die als Anwendungen auf Systemebene initialisiert werden, werden nach dem Initialisieren von Writern als Anwendungen auf Front-End-Ebene oder als Anwendungen auf Back-End-Ebene benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="51084-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="51084-159">Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Back-End-Anwendungen*](vssgloss-b.md), Anwendungen auf [*Front-End-Ebene*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="51084-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="51084-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**Systemanbieter**</span><span class="sxs-lookup"><span data-stu-id="51084-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="51084-161">Der vorinstallierte Standardanbieter, der als Teil von Windows bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="51084-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="51084-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Ordner "System Volume"**</span><span class="sxs-lookup"><span data-stu-id="51084-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="51084-163">Ein frei gegebenes Verzeichnis, in dem die freigegebenen Kopien der öffentlichen Dateien einer Domäne gespeichert werden, d. –. die Dateien, die von allen Domänen Controllern in der Domäne repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="51084-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



