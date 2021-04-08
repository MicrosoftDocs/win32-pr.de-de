---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751537"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="4fa4d-103">I (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="4fa4d-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="4fa4d-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="4fa4d-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4fa4d-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Ereignis ermitteln**</span><span class="sxs-lookup"><span data-stu-id="4fa4d-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="4fa4d-106">Ein VSS-Ereignis, das angibt, dass ein Writer oder eine Anforderer den aktuellen Writer Abfragen muss.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="4fa4d-107">Sie wird verwendet, um die Metadateninformationen des aktuellen Writers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="4fa4d-108">Siehe auch [*anfordernde Person*](vssgloss-r.md), [*Writer*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="4fa4d-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fa4d-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implizite Komponenten Einbindung**</span><span class="sxs-lookup"><span data-stu-id="4fa4d-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="4fa4d-110">Das Hinzufügen von Informationen zu einer Komponente zum Sicherungs Komponenten Dokument eines Anforderers, wenn es an einem Sicherungs-oder Wiederherstellungs Vorgang beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="4fa4d-111">Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger werden nur implizit eingeschlossen, wenn ihr Vorgänger eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="4fa4d-112">Auswählbare Komponenten mit einem auswählbaren Vorgänger können implizit eingeschlossen werden, wenn der Vorgänger eingeschlossen ist oder explizit eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="4fa4d-113">Nicht auswählbare Komponenten ohne auswählbare Vorgänger sind nicht implizit in einem Sicherungs-oder Wiederherstellungs Vorgang enthalten – alle Komponenten müssen explizit dem Dokument mit den Sicherungs Komponenten hinzugefügt werden, wenn eine der Komponenten des Writers beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="4fa4d-114">Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anforderer für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt werden, können nicht implizit in den Vorgang eingeschlossen werden, sondern müssen explizit dem Sicherungs Komponenten Dokument hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="4fa4d-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="4fa4d-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**inkrementelle Sicherungs**</span><span class="sxs-lookup"><span data-stu-id="4fa4d-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="4fa4d-116">Ein Sicherungs-oder Wiederherstellungs Vorgang wird nur für Dateien ausgeführt, die seit der letzten vollständigen, inkrementellen oder differenziellen Sicherung erstellt oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="4fa4d-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="4fa4d-117">Siehe auch [*differenzielle Sicherungs Vorgänge*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="4fa4d-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



