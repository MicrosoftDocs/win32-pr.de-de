---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343682"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="daf7c-103">E (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="daf7c-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="daf7c-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="daf7c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="daf7c-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explizite Komponenten Einbindung**</span><span class="sxs-lookup"><span data-stu-id="daf7c-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="daf7c-106">Das Hinzufügen der Informationen einer Komponente zum Sicherungs Komponenten Dokument eines Anforderers, wenn es an einem Sicherungs-oder Wiederherstellungs Vorgang beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="daf7c-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="daf7c-107">Anforderer verwenden [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , um eine Komponente explizit in einen Sicherungs Vorgang einzubeziehen, und [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) oder [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) , um explizit eine Komponente in einen Wiederherstellungs Vorgang einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="daf7c-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="daf7c-108">Wenn eine beliebige Komponente eines Writers gesichert oder wieder hergestellt wird, müssen alle nicht auswählbaren Komponenten ohne auswählbare Vorgänger explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="daf7c-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="daf7c-109">Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anforderer für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt wurden, müssen explizit in den Vorgang eingeschlossen</span><span class="sxs-lookup"><span data-stu-id="daf7c-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="daf7c-110">Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger werden nie explizit eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="daf7c-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="daf7c-111">Auswählbare Komponenten mit einem auswählbaren Vorgänger können explizit eingeschlossen werden oder implizit eingeschlossen werden, wenn der Vorgänger explizit eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="daf7c-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="daf7c-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**offengelegte Schatten Kopie**</span><span class="sxs-lookup"><span data-stu-id="daf7c-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="daf7c-113">Eine Volumeschattenkopie, die auf einem System bereitgestellt wird und für andere Prozesse als die zur Verfügung steht, die Sie verwaltet.</span><span class="sxs-lookup"><span data-stu-id="daf7c-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="daf7c-114">Ein Schattenkopievolume, das unter einem Laufwerk Buchstaben oder einem Verzeichnis Speicherort eingebunden ist, wird als "lokal verfügbar gemacht" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="daf7c-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="daf7c-115">Ein über eine Freigabe verfügbarer Schattenkopievolume (mit Ausnahme von Client zugänglichen Schatten Kopien) wird als "Remote verfügbar gemacht" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="daf7c-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="daf7c-116">Alle verfügbar gemachten Schatten Kopien sind auch Schatten Kopien.</span><span class="sxs-lookup"><span data-stu-id="daf7c-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="daf7c-117">Weitere Informationen finden Sie auch auf der [*Client zugänglichen Schatten Kopie*](vssgloss-c.md), [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="daf7c-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



