---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344446"
---
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="d5ee7-103">R (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="d5ee7-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d5ee7-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d5ee7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d5ee7-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**anfordernde Person**</span><span class="sxs-lookup"><span data-stu-id="d5ee7-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="d5ee7-106">Mindestens ein Prozess, der mit VSS interagiert, um Schatten Kopien und schattenkopiesätze von einem oder mehreren Volumes zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="d5ee7-107">Normalerweise verwaltet eine anfordernde Person Schatten Kopien, um andere Funktionen zu unterstützen, z. b. Sicherungs-und Wiederherstellungs Vorgänge und Datenträger Spiegelung.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="d5ee7-108">Siehe auch [*Schatten Kopie*](vssgloss-s.md), [*Schattenkopiesatz*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d5ee7-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5ee7-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Restore-Methode**</span><span class="sxs-lookup"><span data-stu-id="d5ee7-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="d5ee7-110">Eine Spezifikation der Wiederherstellungsprozess Methode.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-110">A specification of the restore process method.</span></span> <span data-ttu-id="d5ee7-111">Es steuert solche Probleme, als ob Dateien bei der Wiederherstellung überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="d5ee7-112">Wenn eine Wiederherstellungsmethoden Einstellung mit denen des Wiederherstellungs Ziels in Konflikt steht, hat das Wiederherstellungs Ziel Vorrang.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="d5ee7-113">Siehe auch *Restore Target*.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="d5ee7-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**Wiederherstellungs Ziel**</span><span class="sxs-lookup"><span data-stu-id="d5ee7-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="d5ee7-115">Unter VSS ist ein Wiederherstellungs Ziel eine Angabe, wie ein Anforderer eine Datei wiederherstellen soll, z. b. wenn vorhandene Dateien überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5ee7-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



